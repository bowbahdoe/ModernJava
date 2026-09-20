# Floating Point Numbers

If you expect someone to type a floating point value you can turn the `String`
you get from `IO.readln` into a `double` using `Double.parseDouble`.

```java,no_run
void main() {
    String gpaString = IO.readln("What is your GPA? ");
    double gpa = Double.parseDouble(gpaString);
    IO.println("Your GPA is " + gpa);
}
```

So long as they type something which can be interpreted as a `double` (like `123` or `14.5`) 
you will get a value for the `double` variable. Otherwise, the program will crash.
