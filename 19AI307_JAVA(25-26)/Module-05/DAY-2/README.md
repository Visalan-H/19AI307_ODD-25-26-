# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## AIM:
To do Serialization and Deserialization

## ALGORITHM :
1.	Create a class that implements `Serializable` to allow object conversion.  
2. Build an `ObjectOutputStream` linked to a file and write the object to serialize it.  
3. Close the output stream once writing is done.  
4. Build an `ObjectInputStream` linked to the same file and read the object back.  
5. Cast the returned object to its original type and use it as needed.

#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:
Program to implement a Serialization and Deserialization using Java

## SOURCE CODE:

import java.io.*;

// A simple class that supports serialization
class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class SerializationDemo {
    public static void main(String[] args) {
        String filename = "student.ser";

        // ----- Serialization -----
        try (ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream(filename))) {
            Student s = new Student("Alex", 21);
            out.writeObject(s);
            System.out.println("Object serialized.");
        } catch (IOException e) {
            System.out.println("Serialization error: " + e);
        }

        // ----- Deserialization -----
        try (ObjectInputStream in = new ObjectInputStream(new FileInputStream(filename))) {
            Student s = (Student) in.readObject();
            System.out.println("Object deserialized.");
            System.out.println("Name: " + s.name + ", Age: " + s.age);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Deserialization error: " + e);
        }
    }
}

## OUTPUT:

Object serialized.
Object deserialized.
Name: Alex, Age: 21

## RESULT:

Program executed successfully.
