# Challenges

At the end of each larger section, I am going to write down some things you can do
to make sure you get what was just gone over.

The rules for this are

* Try to use only the information given up to this point in this book.
* Try not to give up until you've given it a solid attempt

## Challenge 1

Write a program that prints your name twice. So if your name is "Jasmine", the output of the program should be this.

```text
Jasmine
Jasmine
```

## Challenge 2

What will this program output when run? Write down your guess and then try actually running it.

~IF toplevel_anonymous_class

```text
void main() {
    System.out.println("A");
    //System.out.println("B");
    System.out.println("C");//
    System.out.println("D");
    /*
    System.out.println("E");
    System.out.println("F");*/
    System.out.println("G");
}
```

~ELSE

```text
public class Main {
    public static void main(String[] args) {
        System.out.println("A");
        //System.out.println("B");
        System.out.println("C");//
        System.out.println("D");
        /*
        System.out.println("E");
        System.out.println("F");*/
        System.out.println("G");
    }
}
```

~ENDIF 




## Challenge 3

There are four semicolons in this perfectly functional program. Delete one of them at random and see what the errors you get look like.

How could you use that error to figure out where you might have forgotten to put a semicolon?

~IF toplevel_anonymous_class

```java
void main() {
    System.out.println("Apple");
    System.out.println("Banana");
    System.out.println("Clementine");
    System.out.println("Durian");
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Apple");
        System.out.println("Banana");
        System.out.println("Clementine");
        System.out.println("Durian");
    }
}
```

~ENDIF