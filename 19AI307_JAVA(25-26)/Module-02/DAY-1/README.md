# Ex.No:2(A) CLASS AND OBJECT

## AIM:

Create a class representing an animal and use objects to access its data and behavior.

## ALGORITHM :

1. Start the program.
2. Define a class with properties and a method.
3. Create an object of that class inside the main method.
4. Assign values to the object’s properties.
5. Call the method to display the animal’s details.

#### Developed By: Visalan H

#### Register Number: 212223240183

## PROGRAM:

### to implement a Class and Objects using Java

## SOURCE CODE:

```java
class Animal {
    String name;
    String sound;

    void makeSound() {
        System.out.println(name + " says " + sound);
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Animal();
        dog.name = "Dog";
        dog.sound = "Woof";

        dog.makeSound();
    }
}
```

## OUTPUT:

```
Dog says Woof
```

## RESULT:
Program executed successfully.
