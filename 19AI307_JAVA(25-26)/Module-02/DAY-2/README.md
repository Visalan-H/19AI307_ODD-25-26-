# Ex.No:2(B) METHODS

## AIM:

Demonstrate how methods define behaviors for objects using a simple animal example.

## ALGORITHM :

1. Start the program.
2. Create a class with one or more methods.
3. Create an object of that class.
4. Call the methods through the object.
5. Display the results.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### to implement a Methods using Java

## SOURCE CODE:

```java
class Animal {
    void eat() {
        System.out.println("The animal is eating.");
    }

    void speak() {
        System.out.println("The animal makes a sound.");
    }
}

public class Msin {
    public static void main(String[] args) {
        Animal cat = new Animal();
        cat.eat();
        cat.speak();
    }
}
```

## OUTPUT:

```
The animal is eating.
The animal makes a sound.
```

## RESULT:

Program executed successfully.
