# Unicode

At the lowest level, computers only work with numbers and have no comprehension of text. A Java `char` is just a number between 0 and 65535. To work with text, we need to agree how to represent strings as numbers.

The good news is that there is an international standard for encoding strings as numbers, called [Unicode](https://en.wikipedia.org/wiki/Unicode), and everyone, including Java, has agreed to follow it.

The bad news is that Unicode is complicated, because human writing is complicated.

Unicode represents text as sequences of numbers called *code points*. As long as you only work with European languages, including English, you can pretend that a code point is just a Java `char`. For example, the letter *D* is assigned to code point 68, so the following are equivalent:

```java
~void main() {
char letterD = 'D';
char alsoLetterD = 68;
IO.println(letterD == alsoLetterD); // true
~}
```

However, not all Unicode code points fit into a `char`. A `char` can only have values between 0 and 65535, but Unicode code points can have values between 0 and 1,114,111. For example, the emoji 👨‍🍳 (code point 128104) cannot be represented by a single `char`:

```java,no_run,does_not_compile
char chef = '👨‍🍳'; // Does not compile
```

Code points that cannot fit into a single `char` are represented as two `char`s, according to the rules of the Unicode encoding called [UTF-16](https://en.wikipedia.org/wiki/UTF-16), which Java uses. UTF-16 specifies the rules for encoding Unicode text as sequences of integers between 0 and 65535 (i.e. `char` values).

Another wrinkle is that a code point does not necessarily correspond to a single character shown on screen. For example, the flag of the European Union 🇪🇺 looks like a single character on screen, but is actually composed of two code points: 🇪 and 🇺 (code points 127466 and 127482 respectively).

Because of these gotchas, you should only work with individual `char` values if you know what you're doing. Most of the time, you will work with whole strings, which are the topic of the [next section](/strings.html).

To get a basic understanding of character encodings, you can read Joel Spolsky's *[The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!)](https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/)*.

UTF-16, used by Java, is not the only way of encoding Unicode as a stream of bytes. Another, far more popular encoding is [UTF-8](https://en.wikipedia.org/wiki/UTF-8), which is used by most web pages. Java uses UTF-16 to represent strings internally, but uses UTF-8 for input/output by default.

For a full explanation of UTF-8, refer to this old Computerphile video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/MijmeoH9LT4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
