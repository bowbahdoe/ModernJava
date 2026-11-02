# Equality

You can check if two `String`s have the same contents by using `.equals`.

```java
~void main() {
String lyricOne = "Green, Green, Dress";
String lyricTwo = "Green, Green, Dress";

boolean areSameLyric = lyricOne.equals(lyricTwo);
boolean isMyName = lyricOne.equals("Bop Bop");

IO.println(areSameLyric);
IO.println(isMyName);
~}
```

You write one `String` on the left, `.equals`, and then the `String` you want to check it
against inside of parentheses.

To see if strings have different contents, you need to use the not operator (`!`) on
the result of `.equals`.

```java
~void main() {
String bow = "bow";
String wow = "WOW";

boolean areNotSame = !bow.equals(wow);

IO.println(areNotSame);
~}
```

Note that you should **not** use `==`. Java will let you do it but you won't get what you expect.[^inaway]

[^inaway]: It is confusing in a way that we aren't ready to explain yet. Just remember for `int`, `double`, `char`, etc. you can use `==`. For `String` use `.equals`. Though, `==` should also not be used to compare `double` as discussed earlier.
