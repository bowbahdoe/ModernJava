# Abstract Methods

Methods on an `abstract` class may themselves be marked `abstract`.

```java
abstract class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    // All classes which extend BodyOfWater must
    // define what happens when you swim.
    abstract void swim();
}
```

Any non-abstract class extending from an `abstract` class must give a definition
for `abstract` methods.

```java
abstract class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    abstract void swim();
}

class Lake extends BodyOfWater {
    // If you didn't define this it wouldn't work
    @Override
    void swim() {
        IO.println("Relaxing time");
    }
}
```

But if an abstract class is being extended by another abstract class, you don't need to.

```java,no_run
abstract class Liquid {
    abstract double viscosity();
}

// Water doesn't need to define viscosity()
// because Water is abstract
abstract class Water extends Liquid {
    abstract double purity();
}

// But as soon as you get to a "concrete" implementation
// you need to provide definitions
class TownWater extends Water {
    @Override
    double viscosity() {
        return 0.01;
    }

    @Override
    double purity() {
        return 0.99;
    }
}
```
