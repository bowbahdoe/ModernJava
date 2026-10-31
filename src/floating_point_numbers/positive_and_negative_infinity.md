# Positive and Negative Infinity

In addition to the wackiness of `NaN`, floating point numbers can also represent both positive
and negative infinity.

You can get positive infinity by dividing any positive number by zero.

```java,no_run
double positiveInfinity = 1.0 / 0.0;
```

You can get negative infinity by dividing any negative number by zero.

```java,no_run
double negativeInfinity = -1.0 / 0.0;
```

As you might expect, positive infinity is greater than any number and negative infinity is less than any number.

```java
~void main() {
~double positiveInfinity = 1.0 / 0.0;
~double negativeInfinity = -1.0 / 0.0;
// true
IO.println(positiveInfinity > 99999999);

// true
IO.println(negativeInfinity < -99999999);
~}
```

Except for `NaN`, of course.

```java
~void main() {
~double positiveInfinity = 1.0 / 0.0;
~double negativeInfinity = -1.0 / 0.0;
double nan = 0.0 / 0.0;

// false
IO.println(positiveInfinity > nan);

// false
IO.println(negativeInfinity < nan);
~}
```
