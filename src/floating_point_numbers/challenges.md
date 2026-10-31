# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    double x = 5.1;
    double y = 2.4;
    IO.println(x + y);
}
```

## Challenge 2

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    double x = 5.1;
    double y = 2.1;
    IO.println(x - y);
}
```

## Challenge 3

What will this program output when run? Write down your guess and then try running it.

How can you make it give the "right" answer?

```java,editable
void main() {
    double x = 5 / 2;
    IO.println(x);
}
```

## Challenge 4

These two expressions give different results. Why is that, and what results do they give?

```java,editable
void main() {
    double resultOne = (int) 5.0 / 2 + 5.0 / 2;
    double resultTwo = (int) (5.0 / 2 + 5.0 / 2);

    IO.println(resultOne);
    IO.println(resultTwo);
}
```

## Challenge 5

The following is a quadratic equation.

\\[ 2x^2 + 8x + 3 = 0 \\]

To find the solutions of any quadratic equation you can use the following formula.

\\[ x = \frac{-b \pm \sqrt{b^2 - 4ac} }{2a} \\]

Where \\(a\\), \\(b\\), and \\(c\\) are the prefixes of each term in the following equation.

\\[ ax^2 + bx + c = 0 \\]

Write some code that finds both solutions to any quadratic equation defined by some variables
`a`, `b`, and `c`. If the equation has imaginary solutions, you are allowed to just output `NaN`.

```java,editable
void main() {
    // For this one in particular, you should output
    // -0.41886116991581 and -3.5811388300842
    // but your code should work with these three numbers changed to
    // represent any given quadratic equation.
    double a = 2;
    double b = 8;
    double c = 3;

    double resultOne = ???;
    double resultTwo = ???;

    IO.println(resultOne); // -0,418861
    IO.println(resultTwo); // -3,581139
}
```

