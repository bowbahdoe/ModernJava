# Relation to Interfaces

When you implement an interface, the implementing class guarentees a contract
and may inherit some default implementations of methods.

```java
// All implementing classes must define a run method
interface Runner {
    void run();

    default void runFar() {
        run();
        run();
        run();
    }
}

class RoadRunner implements Runner {
    @Override
    public void run() {
        IO.println("meep meep");
    }
}

class Main {
    void main() {
        Runner r = new RoadRunner();
        r.runFar();
    }
}
```

This is also true when extending a class. The difference is that you may inherit
fields, behavior dependent on fields, and actual constructors.

```java
abstract class Swimmer {
    private int laps = 0;

    public abstract void swim();

    // The inherited behavior may depend on fields
    public void swimFar() {
        IO.println("lap: " + laps);
        swim();
        laps++;

        IO.println("lap: " + laps);
        swim();
        laps++;

        IO.println("lap: " + laps);
        swim();
        laps++;
    }
}

class Person extends Swimmer {
    @Override
    public void swim() {
        IO.println("*gasps for air*");
    }
}

class Main {
    void main() {
        Swimmer s = new Person();
        s.swimFar();
    }
}
```

Because of these differences while it is possible to implement many interfaces, a
class can only extend from exactly one other class.[^somelangs]

Because of these differences, the general consensus is that interfaces are the mechanism to use
for abstracting behavior. Abstract classes, by contrast, should be used primarily to reduce duplicated code.[^tricky]

[^somelangs]: Some languages do allow for "multiple inheritance." Doing so leads to some wacky and hard to think about things so Java doesn't allow it.

[^tricky]: It's a little tricky because both interfaces and abstract classes can be used for similar things. A "pure abstract class" - a class with nothing but a bunch of abstract methods - is very close in
concept to an interface. If its all still confusing to you then just ignore everything but interfaces.

