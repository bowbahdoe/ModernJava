# First Steps

If you made it through the [Getting Started section](./getting_started/hello_world.md) you've successfully run this program.

~IF toplevel_anonymous_class

```java
void main() {
    System.out.println("Hello, World!");
}
```

~ELSE 

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

~ENDIF

This "prints" - not in the sense of a physical printer, but like "displays on the screen" -
the text `"Hello, World!"`.

Its a tradition for this to be your first program in any language.
~IF toplevel_anonymous_class

We aren't quite at the point where I can explain what `void main()` means, but
all you need to know for now is that it is what Java looks for to know where to start the program.

```java
void main() {
    < WRITE YOUR CODE HERE >
}
```


~ELSE

Unfortunately, for reasons that are impossible to explain with the context you have at this point,
half of this probably reads as cryptic nonsense.

```java
public class Main {
    public static void main(String[] args) {
```

I don't _want_ it to stay cryptic nonsense, but until we get there all you truly need to know
is that Java uses all of that to know where to start the program.

```java
public class Main {
    public static void main(String[] args) {
        < WRITE YOUR CODE HERE >
    }
}
```

~ENDIF

So for all intents and purposes, this is the whole program.

```java
System.out.println("Hello, World!");
```

This bit of magic here - `System.out.println` - is a "statement" that "prints" the text inside the `(` and `)` as well as a "new line" to the screen.

`print` with new `l`i`n`e.

If you were to replace it with `System.out.print`, then the output would lack that new line. This makes the following program be functionally identical to the first.

```java
System.out.print("Hello, ");
System.out.print("World");
System.out.println("!");
```

~IF toplevel_anonymous_class

Which, when we add back `void main()`, looks like this.

```java
void main() {
    System.out.print("Hello, ");
    System.out.print("World");
    System.out.println("!");
}
```

~ELSE

Which, when we add back the part you are squinting past, looks like this.

```java
public class Main {
    public static void main(String[] args) {
        System.out.print("Hello, ");
        System.out.print("World");
        System.out.println("!");
    }
}
```

~ENDIF



You should get in the habit of, whenever you see some bit of code, trying to physically type it out, run it,
tweak it, and play with it.

So try playing around with this program. If you are not actively engaging then the whole thing is a bit of a wash.
