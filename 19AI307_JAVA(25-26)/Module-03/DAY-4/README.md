# Ex.No:3(C) ABSTRACTION

## AIM:
Show how abstraction hides implementation details using an abstract class.

## ALGORITHM :
1. Start the program.
2. Create an abstract class with an abstract method.
3. Create a subclass that implements the abstract method.
4. Create an object of the subclass in the main method.
5. Call the implemented method and display the output.
6. 
#### Developed By: Visalan H
#### Register Number: 212223240183
## PROGRAM:
### to implement a Abstraction using Java


## SOURCE CODE:

```java
abstract class Animal {
    abstract void sound();
}

class Cow extends Animal {
    void sound() {
        System.out.println("Cow moos");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Cow();
        a.sound();
    }
}
```





## OUTPUT:
```
Cow moos
```


## RESULT:
