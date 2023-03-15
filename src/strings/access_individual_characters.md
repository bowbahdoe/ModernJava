# Access Individual Characters

Given a `String`, you can access the individual characters which
comprise it by using `.charAt`.


The first character can be accessed by putting `0` in the parentheses.
The second by using `1`, and so on.

```java
String spy = "loid";

char l = spi.charAt(0);
System.out.println(l);

char o = spi.charAt(1);
System.out.println(o);

char i = spi.charAt(2);
System.out.println(i);

char d = spi.charAt(3);
System.out.println(d);
```

We call this number the "index" of the character.[^otherds] 

The index of the character to access can come from a variable.

```java
String assassin = "yor";
int indexOfR = 2;

char r = assassin.charAt(indexOfR);
System.out.println(r);
```


If you give a number equal to or greater than the lenth of the `String` or a number less than zero,
you will get an error.

```java
String student = "anya";
// Crash!
student.charAt(999);
```

```java
String dog = "bond";
// Crash!
dog.charAt(-1);
```

[^otherds]: There will be more things
which have their individual elements accessible by indexes. They will all generally start from 0 for the first element
but there are rare exceptions. 