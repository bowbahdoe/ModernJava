# Formatting

You may have noticed that after each `{` all the code that comes after it is "indented" in one "level."

~IF toplevel_anonymous_class

```java
void main() {
    System.out.println("Hello, World!");
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

~ENDIF

~IF toplevel_anonymous_class

~ELSE

Then, when there is a `}` everything is "de-dented" one level.

~ENDIF


I will kindly ask that you try to stick to this rule when writing your own code as well.
If you try to find help online and you haven't, it will be hard for people
to read your code.

This is easier to show than to explain in detail. Just try to make your code look like this.

✅
~IF toplevel_anonymous_class

```java
void main() {
    System.out.println("Hello, World!");
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
~ENDIF


And not like this.

❌

~IF toplevel_anonymous_class

```java
void main() 
{
System.out.println("Hello, World!");}
```

~ELSE 

```java
public class Main 
    {
    public static void main(String[] args) 
            {
        System.out.println("Hello, World!");
            }
    }
```

~ENDIF

And keep in mind that this rule of thumb applies to every language constrict that requires a `{` and `}` many of which I will introduce later.
