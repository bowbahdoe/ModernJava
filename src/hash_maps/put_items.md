# Put Items

Putting it all together[^getit], we can "put"
items into our hash map by following these steps.

1. Compute the hash code of the key.
2. Find the bucket that item should go in based on the key.
3. Add the item to the bucket.

```java
record CarsCharacter(
    String firstName, 
    String lastName
) {}

class Bucket {
    private CarsCharacter[] data;
    private int size;

    Bucket() {
        this.data = new CarsCharacter[0];
        this.size = 0;
    }

    CarsCharacter get(int index) {
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        return this.data[index];
    }

    void set(int index, CarsCharacter value) {
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        this.data[index] = value;
    }

    int size() {
        return this.size;
    }

    void add(CarsCharacter value) {
        if (size >= this.data.length - 1) {
            int newLength = this.data.length * 2;
            if (newLength == 0) {
                newLength = 2;
            }

            CarsCharacter[] newArray = new CarsCharacter[newLength];
            for (int i = 0; i < this.data.length; i++) {
                newArray[i] = this.data[i];
            }
            this.data = newArray;
        }

        this.data[size] = value;
        this.size++;
    }
}



class CarsCharacterHashMap {
    Bucket[] buckets = new Bucket[] {
        new Bucket(),
        new Bucket(),
        new Bucket()
    };

    int indexFor(char hash) {
        if (hash >= 'A' && hash <= 'F') {
            return 0;
        }
        else if (hash >= 'G' && hash <= 'N') {
            return 1;
        }
        else {
            return 2;
        }
    }

    char hashFunction(
        String lastName
    ) {
        return lastName.charAt(0);
    }

    void put(String lastName, CarsCharacter character) {
        // 1. Compute the hash code
        char hash = hashFunction(lastName);
        // 2. Find the bucket
        Bucket bucket = buckets[indexFor(hash)];
        // 3. Add to the bucket
        bucket.add(character);
    }
}

void main() {
    var map = new CarsCharacterHashMap();

    map.put("Carrera", new CarsCharacter("Sally", "Carrera"));
    map.put("Hudson", new CarsCharacter("Doc", "Hudson"));
    map.put("McQueen", new CarsCharacter("Lightning", "McQueen"));

    System.out.println(map.buckets[0].size());
    System.out.println(map.buckets[1].size());
    System.out.println(map.buckets[2].size());
}
```


[^getit]: ayy