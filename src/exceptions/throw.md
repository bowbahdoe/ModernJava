# throw

In order to throw an exception from your own code, you say `throw`, `new`, then the name
of the exception and `()`.

`RuntimeException` is one of many kinds of exceptions, but you can get by with just that one for a bit.

```java,panics
void crashesOnFive(int x) {
    if (x == 5) {
        throw new RuntimeException();
    }
}

void main() {
    crashesOnFive(1);
    IO.println("Made it to step 1");

    crashesOnFive(5);
    IO.println("Will not make it to step 2");
}
```