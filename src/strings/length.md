# Length

The number of `char`s which comprise a `String` can be accessed by using `.length()`.[^codepoints]

```java
String fruit = "strawberry";
int numberOfChars = fruit.length();

// strawberry is 10 characters long
System.out.println(
    fruit + " is " numberOfChars + " characters long"
);
```

[^codepoints]: This is different from the number of unicode codepoints.
