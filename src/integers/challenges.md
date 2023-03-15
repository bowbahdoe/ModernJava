# Challenges

Remember the rules for this are

* Try to use only the information given up to this point in this book.
* Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class
```java
void main() {
    int x = 5;
    int y = 8;
    System.out.println(x + y);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        int y = 8;
        System.out.println(x + y);
    }
}
```
~ENDIF



## Challenge 2

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class
```java
void main() {
    int x = 5;
    x--;
    x--;
    x = x + x;
    System.out.println(x);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        x--;
        x--;
        x = x + x;
        System.out.println(x);
    }
}
```
~ENDIF


## Challenge 3

Make it so that this program correctly determines if the numbers are even or not.

Assume that the values of `x`, `y`, and `z` could be changed. Don't just write out
literally `true` and `false` for their current values.

~IF toplevel_anonymous_class
```java
void main() {
    int x = 5;
    int y = 4;
    int z = 98;

    boolean xIsEven = < CODE HERE >;
    System.out.println(xIsEven);

    boolean yIsEven = < CODE HERE >;
    System.out.println(yIsEven);

    boolean zIsEven = < CODE HERE >;
    System.out.println(zIsEven);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        int y = 4;
        int z = 98;

        boolean xIsEven = < CODE HERE >;
        System.out.println(xIsEven);

        boolean yIsEven = < CODE HERE >;
        System.out.println(yIsEven);

        boolean zIsEven = < CODE HERE >;
        System.out.println(zIsEven);
    }
}
```
~ENDIF


## Challenge 4

Try dividing a number by zero. What happens?

Write down your guess and then try running the program below to see.

~IF toplevel_anonymous_class
```java
void main() {
    System.out.println(5 / 0);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        System.out.println(5 / 0);
    }
}
```
~ENDIF


## Challenge 5

What can you write in the spot marked that will make the program output 2?

~IF toplevel_anonymous_class
```java
void main() {
    int x = 5;
    int y = <CODE HERE>;
    System.out.println(x + y);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        int y = <CODE HERE>;
        System.out.println(x + y);
    }
}
```
~ENDIF


## Challenge 6

What is the output of this code.[^fbarticle]

~IF toplevel_anonymous_class
```java
void main() {
    System.out.println(
        6 / 2 * (1 + 2)
    );
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        System.out.println(
            6 / 2 * (1 + 2)
        );
    }
}
```
~ENDIF


[^fbarticle]: [Now get in a fight with your relatives about it](https://slate.com/technology/2013/03/facebook-math-problem-why-pemdas-doesnt-always-give-a-clear-answer.html)
