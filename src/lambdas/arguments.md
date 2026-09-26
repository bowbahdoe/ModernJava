# Arguments

If the method on the functional interface takes arguments
you can include those in the parentheses before the `->`.

```java
@FunctionalInterface
interface Singer {
    void sing(String title, double volume);
}

class Main {
    void main() {
        Singer woodkid = (String title, double volume) -> {
            IO.println(
                title 
                    + " by woodkid is now " 
                    + (volume > 10 ? "BLASTING" : "playing"
                )
            );
        };

        // AC Revelations wasn't the best game
        // but that trailer was awesome.
        woodkid.sing("Iron", 11);
    }
}
```

If it won't lead to any ambiguity Java also allows you to omit the types
from the argument list.

```java
@FunctionalInterface
interface Singer {
    void sing(String title, double volume);
}

class Main {
    void main() {
        Singer twrp = (title, volume) -> {
            IO.println(
                title 
                    + " by twrp is now " 
                    + (volume > 10 ? "BLASTING" : "playing"
                )
            );
        };

        twrp.sing("Pets", 7);
    }
}
```

Further, if there is only one argument you may omit even the `()`.

```java
@FunctionalInterface
interface Conductor {
    void conduct(String tempo);
}

class Main {
    void main() {
        Conductor jkSimmons = tempo -> IO.println("Not my tempo.")

        jkSimmons.conduct("4/4");
    }
}
```