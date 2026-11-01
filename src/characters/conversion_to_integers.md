# Conversion to Integers

All `char`s have a matching numeric value[^ascii]. `'a'` is `97`, `'b'` is `98`,
`'&'` is `38`, and so on.

Same as assigning an `int` to a `double`, you can perform a widening conversion
by attempting to assign a `char` to an `int`.

```java
~void main() {
int valueOfA = 'a';

IO.println(valueOfA);
~}
```

`char`s will be automatically converted to `int`s when used with mathmatical operators like `+`, `-`, `>`, `<`, etc.

```java
~void main() {
char gee = 'g';

// all the letters from a to z have consecutive numeric values.
boolean isLetter = 'a' <= gee && gee <= 'z';

IO.println(isLetter);
~}
```

This can be useful if you are stranded on Mars[^onmars] or
if you want to see if a character is in some range.

[^ascii]: You can find some of these values in an "[ASCII Table](https://www.ascii-code.com/)."

[^onmars]: [https://www.youtube.com/watch?v=0xkP_FQUsuM](https://www.youtube.com/watch?v=0xkP_FQUsuM)
