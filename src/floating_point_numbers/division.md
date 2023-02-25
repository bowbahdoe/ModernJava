# Division

You can divide any two `double`s using the `/` operator.

```java
double x = 8;
// y will be 4.0
double y = x / 2;
// z will be 1.3333333333333333
double z = y / 3;

System.out.println(x);
System.out.println(y);
System.out.println(z);
```

Unlike with integer division, floating point division will include the remainder in the result.[^caveat]

[^caveat]: With the caveat that the result is now potentially inaccurate.
