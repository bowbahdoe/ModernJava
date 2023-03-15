# Challenges

Remember the rules for this are

* Try to use only the information given up to this point in this book.
* Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class
```java
void main() {
    boolean a = true;
    boolean b = false;
    boolean c = true;
    boolean d = false;

    boolean result = a || b && c || !d;

    System.out.println(result);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        boolean a = true;
        boolean b = false;
        boolean c = true;
        boolean d = false;

        boolean result = a || b && c || !d;

        System.out.println(result);
    }
}
```
~ENDIF



## Challenge 2

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class
```java
void main() {
    boolean a = true;
    boolean b = false;
    boolean c = true;
    boolean d = false;

    boolean result = !(a || b && c || !d) || (a && b || c);

    System.out.println(result);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        boolean a = true;
        boolean b = false;
        boolean c = true;
        boolean d = false;

        boolean result = !(a || b && c || !d) || (a && b || c);

        System.out.println(result);
    }
}
```
~ENDIF


## Challenge 3

Say you have two boolean variables, how could you use the operators we've covered to get the "exclusive or" of the two.

~IF toplevel_anonymous_class
```java
void main() {
    // Change these two variables to test your solution
    boolean hasIceCream = true;
    boolean hasCookie = false;

    boolean validChoice = < YOUR CODE HERE >;

    System.out.println(validChoice);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        // Change these two variables to test your solution
        boolean hasIceCream = true;
        boolean hasCookie = false;

        boolean validChoice = < YOUR CODE HERE >;

        System.out.println(validChoice);
    }
}
```
~ENDIF


Make sure to test all the possibilities.

| hasIceCream | hasCookie | validChoice |
|-------------|-----------|-------------|
| true        | true      | false       |
| true        | false     | true        |
| false       | true      | true        |
| false       | false     | false       |
