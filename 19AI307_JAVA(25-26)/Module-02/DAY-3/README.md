# Ex.No:2(C) ACCESS SPECIFIERS

## AIM:

Demonstrate how different access specifiers control visibility of class members.

## ALGORITHM :

1. Start the program.
2. Create a class with variables/methods using different access specifiers.
3. Create an object of the class in the main program.
4. Access the allowed members through the object.
5. Display the results.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### implement a Access Specifiers using Java

## SOURCE CODE:

```java
class Animal {
    public String name = "Lion";
    private int age = 5;
    protected String sound = "Roar";

    public void showName() {
        System.out.println("Name: " + name);
    }

    private void showAge() {
        System.out.println("Age: " + age);
    }

    protected void makeSound() {
        System.out.println("Sound: " + sound);
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Animal();
        a.showName();
        a.makeSound();
    }
}
```

## OUTPUT:

```
Name: Lion
Sound: Roar
```

## RESULT:

Program executed successfully.
