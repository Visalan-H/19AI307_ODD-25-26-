# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## AIM:

Show how variable scope works and how a constructor initializes object data.

## ALGORITHM :

1. Start the program.
2. Create a class with instance variables and a constructor.
3. Use the constructor to initialize the instance variables.
4. Create an object of the class inside the main method.
5. Display the initialized values.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

### to implement a Variable scope and Constructor using Java

## SOURCE CODE:

```java
class Animal {
    String name;
    int age;

    Animal(String n, int a) {
        name = n;
        age = a;
    }

    void display() {
        String info = name + " is " + age + " years old";
        System.out.println(info);
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Animal("Dog", 3);
        dog.display();
    }
}
```

## OUTPUT:

```
Dog is 3 years old
```

## RESULT:

Program executed successfully.
