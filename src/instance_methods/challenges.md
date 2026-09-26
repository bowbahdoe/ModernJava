# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make a class named `PirateShip` which has one `int` field
named `crewSize`.

Add an instance method to that class named `sail` which outputs

```
N sailors, ready to sail!
```

Where *N* is the size of the crew.

```java,editable
// ----------------
// CODE HERE
// ----------------

void main() {
    PirateShip ship = new PirateShip();
    ship.crewSize = 25;
    ship.sail();
}
```

## Challenge 2.

Make a class named `StringArrayView` which has
one `String[]` field named `value`
 and two methods named `get` and `length`.

`get` should take in an index and return the matching element
of the array.

`length` should take no arguments and give the length of the array.

```java,editable
// ----------------
// CODE HERE
// ----------------

void main() {
    StringArrayView view = new StringArrayView();
    view.value = new String[] { "A", "B", "C" };

    // 3
    IO.println(view.length());

    // A
    IO.println(view.get(0));

    // C
    IO.println(view.get(2));
}
```

## Challenge 3.

Alter the `VoiceActor` class so that it has a method named `fullName`
that returns their `firstName` followed by their `lastName` and separated
by a space.

If their `lastName` is `null`, you should have no trailing space.
If their `firstName` is `null`, you should have no leading space.

If both their `firstName` and `lastName` are `null`, you should
return `"No Name"`.

```java,editable
class VoiceActor {
    String firstName;
    String lastName;

    // -----------------
    // CODE HERE
    // -----------------
}

void main() {
    VoiceActor goku = new VoiceActor();
    goku.firstName = "Masako";
    goku.lastName = "Nozawa";

    // "Masako Nozawa"
    String gokuFullName = goku.fullName();
    IO.println(gokuFullName);

    // "Nozawa"
    goku.firstName = null;
    gokuFullName = goku.fullName();
    IO.println(gokuFullName);

    // "No Name"
    goku.lastName = null;
    gokuFullName = goku.fullName();
    IO.println(gokuFullName);

    // "Horikawa"
    VoiceActor vegeta = new VoiceActor();
    vegeta.lastName = "Horikawa";
    IO.println(vegeta.fullName());
}
```

## Challenge 4.

Update the definition for the `Taco` class so that it has a method named
`deluxe`. This should set the taco to have beef, sour cream, cheese,
and onion. Use the existing instance methods instead of directly accessing
fields.

```java,editable
class Taco {
    boolean beef;
    boolean sourCream;
    boolean cheese;
    boolean onion;

    void addBeef() {
        this.beef = true;
    }

    void addSourCream() {
        this.sourCream = true;
    }

    void addCheese() {
        this.cheese = true;
    }

    void addOnion() {
        this.onion = true;
    }

    void deluxe() {
        // ------------
        // CODE HERE
        // ------------
    }
}

void main() {
    var taco = new Taco();
    taco.deluxe();

    IO.println("Has Beef: " + taco.beef);
    IO.println("Has Sour Cream: " + taco.sourCream);
    IO.println("Has Cheese: " + taco.cheese);
    IO.println("Has Onion: " + taco.onion);
}
```

## Challenge 5.

Why doesn't this code function as you'd expect? Fix it by changing one line.

```java,editable
class Oscar {
    boolean grouchy;

    void setGrouchy(boolean grouchy) {
        grouchy = grouchy;
    }
}

void main() {
    var oscar = new Oscar();
    oscar.setGrouchy(true);
    IO.println(oscar.grouchy);
}
```

## Challenge 6.

Make a `Rectangle` class which has a `width` field and a `height`
field. Give it an instance method named `toCharArray` which gives
a `char[]` that can be printed to display a rectangle of the given
width and height.

```java,editable
// ------------
// CODE HERE
// ------------

void main() {
    Rectangle rectangle = new Rectangle();
    rectangle.width = 3;
    rectangle.height = 4;

    /*
        ***
        ***
        ***
        ***
    */
    char[] c = rectangle.toCharArray();
    IO.println(c);
}
```
