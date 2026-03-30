# Ex.No:3(E) INNER CLASS

## AIM:

Show how an inner class works inside an outer class and how it can access outer members.

## ALGORITHM :

1. Start the program.
2. Create an outer class with a variable.
3. Create an inner class inside the outer class.
4. Create an object of the inner class using the outer class.
5. Call the inner class method to display the output.

## PROGRAM:

### to implement a InnerClass using Java

## SOURCE CODE:

```java
class Outer {
    String msg = "Hello from Inner Class";

    class Inner {
        void display() {
            System.out.println(msg);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Outer o = new Outer();
        Outer.Inner in = o.new Inner();
        in.display();
    }
}
```

## OUTPUT:

```
Hello from Inner Class
```

## RESULT:

Program executed successfully.
