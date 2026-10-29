# Scope

Within an inner class all fields and methods of the instance it was created in
are available.

```java,no_run
class Car {
    int speed = 0;

    class Speedometer {
        int getSpeed() {
            return speed;
        }
    }

    Speedometer getSpeedometer() {
        return new Speedometer();
    }
}
```
```java,no_run
~class Car {
~    int speed = 0;
~
~    class Speedometer {
~        int getSpeed() {
~            return speed;
~        }
~    }
~
~    Speedometer getSpeedometer() {
~        return new Speedometer();
~    }
~}
class Main {
    void main() {
        Car car = new Car();
        Car.Speedometer speedometer = car.getSpeedometer();
    }
}
```
One mental model for this is that its as if the inner class
holds a reference to the one it was created in.

```java,no_run
class Car {
    int speed = 0;
}

class CarSpeedometer {
    private final Car madeBy;

    CarSpeedometer(Car madeBy) {
        this.madeBy = madeBy;
    }

    int getSpeed() {
        return madeBy.speed;
    }
}
```
