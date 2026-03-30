# Ex.No:3(F) WRAPPER CLASS

## AIM:
Show how wrapper classes convert primitive data types into objects.

## ALGORITHM :
1. Start the program.
2. Declare primitive data types.
3. Convert them into wrapper class objects.
4. Use wrapper class methods to process data.
5. Display the results.


## PROGRAM:
### to implement a Wrapper Class using Java

## SOURCE CODE:


```java
public class Main {
    public static void main(String[] args) {
        int a = 25;
        Integer obj = Integer.valueOf(a);

        double b = 12.5;
        Double obj2 = Double.valueOf(b);

        System.out.println("Integer object: " + obj);
        System.out.println("Double object: " + obj2);
    }
}
```




## OUTPUT:
```
Integer object: 25
Double object: 12.5
```


## RESULT:
