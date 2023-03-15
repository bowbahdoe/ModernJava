# Final Variables

There is an optional extra part to a variable declaration where you can
mark a variable as "final", meaning its value can never be reassigned.

~IF toplevel_anonymous_class
```java
void main() {
    final String coolestChef = "Anthony Bourdain";
    System.out.println(coolestChef);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        final String coolestChef = "Anthony Bourdain";
        System.out.println(coolestChef);
    }
}
```
~ENDIF


If you try to reassign a final variable, Java will not accept your program.

~IF toplevel_anonymous_class
```java
void main() {
    final String coolestChef = "Anthony Bourdain";
    System.out.println(coolestChef);

    // I'm sorry, but no. Cool guy, but no.
    coolestChef = "Gordan Ramsey";
    System.out.println(coolestChef);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        final String coolestChef = "Anthony Bourdain";
        System.out.println(coolestChef);

        // I'm sorry, but no. Cool guy, but no.
        coolestChef = "Gordan Ramsey";
        System.out.println(coolestChef);
    }
}
```
~ENDIF


This is useful if you have a lot of lines of code and want the mental
comfort of knowing you couldn't have reassigned that variable at any
point between its declaration and its use.

```java
final String genie = "Robin Williams";
// imagine
// 100s of lines
// of code
// and it is 
// hard to
// read all of it
// at a glance
// ......
// ......
// You can still be sure "genie" 
// has the value of "Robin Williams"
System.out.println(genie);
```

Variables whose assignment is delayed can also be marked final.

```java
final String mario;
mario = "Charles Martinet";
```

The restriction is the same - after the initial assignment, the variable
cannot be reassigned.

```java
final String mario;
// An initial assignment is fine
mario = "Charles Martinet";
// But you cannot reassign it afterwards
mario = "Chris Pratt";
```

The downside to this, of course, is more visual noise. If a variable is only
"alive" for a small part of the code, then adding `final` might make it harder
to read the code, not easier.
