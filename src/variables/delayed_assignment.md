# Delayed Assignment

The declaration of a variable and the assignment of its initial value can
be done separately.

~IF toplevel_anonymous_class
```java
void main() {
    String contestWinner;
    contestWinner = "Boaty McBoatface";

    System.out.println(contestWinner);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        String contestWinner;
        contestWinner = "Boaty McBoatface";

        System.out.println(contestWinner);
    }
}
```
~ENDIF


In which case the "variable declaration" will only have the "type" and "name" components.

```java
   String contestWinner;
//  type  name
```

And the "initial assignment" will look identical to a "re-assignment".

```java
   contestWinner = "Boaty McBoatface";
//   name            initial value
```

Before an initial value is assigned to a variable, it is not allowed to be used.[^whydelay]

~IF toplevel_anonymous_class
```java
void main() {
    String contestWinner;
    // This will not run, since Java knows that
    // you never gave contestWinner an initial value.
    System.out.println(contestWinner);
}
```
~ELSE
```java
public class Main {
    public static void main(String[] args) {
        String contestWinner;
        // This will not run, since Java knows that
        // you never gave contestWinner an initial value.
        System.out.println(contestWinner);
    }
}
```
~ENDIF


[^whydelay]: There is no direct use for separating declaration and initial assignment at this point,
but [it's a surprise tool that will help us later](https://knowyourmeme.com/memes/its-a-surprise-tool-that-will-help-us-later).
