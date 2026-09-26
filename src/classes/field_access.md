# Field Access

You can access the value of any field in a class by writing the name of a variable holding an instance
of that class, plus a `.`, then the name of that field.

```java
class Muppet {
    String name;
}

void main() {
    Muppet kermit = new Muppet();
    kermit.name = "Kermit The Frog";

    // The .name accesses the "name" field
    IO.println(kermit.name);
}
```
