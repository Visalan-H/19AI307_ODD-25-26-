# Ex.No:4(C) COMPOSITION IN JAVA

## AIM:

Demonstrate composition by creating a class that contains another class as part of its structure.

## ALGORITHM :

1. Start the program.
2. Create a component class that represents a part of a bigger object.
3. Create a main class that contains an instance of the component class.
4. Initialize the composition in the constructor.
5. Use the composed object to perform actions and display results.

#### Developed By: Visalan H

#### Register Number: 212223240183

## PROGRAM:

### to implement a Composition Concepts in Java

## SOURCE CODE:

```java
class Engine {
    void start() {
        System.out.println("Engine started");
    }
}

class Car {
    private Engine engine;

    Car() {
        engine = new Engine();
    }

    void drive() {
        engine.start();
        System.out.println("Car is moving");
    }
}

public class Main {
    public static void main(String[] args) {
        Car c = new Car();
        c.drive();
    }
}
```

## OUTPUT:

```
Engine started
Car is moving
```

## RESULT:

Program executed successfully.
