# Ex.No:3(b) POLYMORPHISM

## AIM:

Demonstrate polymorphism by allowing multiple animal classes to provide their own version of the same method.

## ALGORITHM :

1. Start the program.
2. Create a base class with a method.
3. Create subclasses that override the method.
4. Store subclass objects in a base-class reference.
5. Call the method to show different behaviors.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### to implement a Polymorphism using Java

## SOURCE CODE:

```java
class Animal {
    void speak() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void speak() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    void speak() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a1 = new Dog();
        Animal a2 = new Cat();

        a1.speak();
        a2.speak();
    }
}

```

## OUTPUT:

```
Dog barks
Cat meows
```

## RESULT:

Program executed successfully.
