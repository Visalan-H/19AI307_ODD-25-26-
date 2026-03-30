# Ex.No:3(A) INHERITANCE AND AGGREGATION

## AIM:

Demonstrate inheritance between shape classes and aggregation by using one class inside another.

## ALGORITHM :

1. Start the program.
2. Create a base class and extend it using a derived class.
3. Create another class that contains an object of a shape class (aggregation).
4. Instantiate objects and use their methods.
5. Display the results.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### to implement a Inheritance and Aggregation using Java

## SOURCE CODE:

```java
class Shape {
    String name;

    Shape(String name) {
        this.name = name;
    }

    void showName() {
        System.out.println("Shape: " + name);
    }
}

class Rectangle extends Shape {
    int length;
    int width;

    Rectangle(int length, int width) {
        super("Rectangle");
        this.length = length;
        this.width = width;
    }

    int area() {
        return length * width;
    }
}

class ShapeInfo {
    Rectangle rect;

    ShapeInfo(Rectangle rect) {
        this.rect = rect;
    }

    void display() {
        rect.showName();
        System.out.println("Area: " + rect.area());
    }
}

public class Main {
    public static void main(String[] args) {
        Rectangle r = new Rectangle(5, 3);
        ShapeInfo info = new ShapeInfo(r);
        info.display();
    }
}
```

## OUTPUT:

```
Shape: Rectangle
Area: 15
```

## RESULT:

Program executed successfully.
