# Challenges

Remember the rules for this are

* Try to use only the information given up to this point in this book.
* Try not to give up until you've given it a solid attempt

## Challenge 1

A lot of math problems ask you to find \\( x^2 \\). What is the value of the character `x` squared?

Try to work it out on paper before running the program below.

~IF toplevel_anonymous_class
```java
void main() {
    char x = 'x';

    System.out.println(x * x);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        char x = 'x';

        System.out.println(x * x);
    }
}
```
~ENDIF


## Challenge 2

Alter the program below so that it will output `true` if the character declared at the top is a letter.

Make use of the fact that the numeric values for `a` - `z` and `A` - `Z` are contiguous.

~IF toplevel_anonymous_class
```java
void main() {
    char c = 'a';

    boolean isLetter = ???;

    System.out.println(isLetter);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        char c = 'a';

        boolean isLetter = ???;

        System.out.println(isLetter);
    }
}
```
~ENDIF


## Challenge 3

How many UTF-16 code units does it take to represent this emoji? `👨‍🍳`.
