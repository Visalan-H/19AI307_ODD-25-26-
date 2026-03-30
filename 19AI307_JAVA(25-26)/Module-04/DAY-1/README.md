# Ex.No:4(A) EXCEPTION HANDLING

## AIM:

Demonstrate how exceptions are caught and handled using try–catch.

## ALGORITHM :

1. Start the program.
2. Place a risky operation inside a try block.
3. Catch the exception using a catch block.
4. Display an error message when an exception occurs.
5. Continue program execution smoothly.

#### Developed By: Visalan H

#### Register Number: 212223240183

## PROGRAM:

### to implement a Exception Handling using Java

## SOURCE CODE:

```java
public class Main {
    public static void main(String[] args) {
        try {
            int x = 10 / 0;
            System.out.println(x);
        } catch (ArithmeticException e) {
            System.out.println("Error: Cannot divide by zero");
        }
    }
}
```

## OUTPUT:

```
Error: Cannot divide by zero
```

## RESULT:

Program executed successfully.
