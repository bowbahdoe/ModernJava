# Hello, World

There are a lot of ways to "get set up" to run Java code.

For the purposes of this book, I am going to reccomend that you
start with [replit.com](https://replit.com).

It requires an internet connection and you will have to make an account, but
of the available options it is the easiest to set up.

If you are in school and your teacher has helped you get set up in some other
way it is okay to skip this section and just do it the way you were shown.

All that matters is that in the end you have the ability to run and
edit the following code.

~IF toplevel_anonymous_class

```java
void main() {
    System.out.println("Hello, World");
}
```

~ELSE


```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World");
    }
}
```

~ENDIF

## Step 1. Make an account

Go to [replit.com](https://replit.com) and find the "Sign Up" button.
Websites change every now and then so these screenshots might be out of date.

<img src="/getting_started/repl_signup_0.png"
     alt="Picture of the sign up button on replit's website"
     width = "200">

Click it and sign up for an account.

<img src="/getting_started/repl_signup_1.png"
     alt="Picture of the sign up form on replit's website"
     width = "200">

## Step 2. Create a Java REPL

Find the "Create REPL" button and click it.

<img src="/getting_started/repl_1.png"
     alt="Picture of the create repl button on replit's website"
     width = "200">

Then you should be presented with a menu that lets you search for the type of REPL to create.
Find the Java template and click "Create".

<img src="/getting_started/repl_2.png"
     alt="Unfilled in create from template menu on replit"
     width = "200">

<img src="/getting_started/repl_3.png"
     alt="Filled in create from template menu on replit"
     width = "200">

## Step 3. Run code

You should land on a screen with a big green run button, an open file called
"Main.java", and a blank window labeled "console".


<img 
~IF toplevel_anonymous_class
     src="/getting_started/repl_4_voidmain.png"
~ELSE
     src="/getting_started/repl_4.png"
~ENDIF
     alt="Picture of an unran hello world program"
     width = "800">

Click it and you should see the text `Hello, world!` appear under the console window.

<img 
~IF toplevel_anonymous_class
     src="/getting_started/repl_5_voidmain.png"
~ELSE
     src="/getting_started/repl_5.png"
~ENDIF
     alt="Picture of a hello world program after running"
     width = "800">

