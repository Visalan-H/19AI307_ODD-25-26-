# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:


## AIM:
Convert an object into a byte stream for storage and later restore it back into a full object.

## ALGORITHM :
1.	Define a class that implements `Serializable` so its objects can be converted to bytes.  
2. Create an `ObjectOutputStream` and write the object to a file to serialize it.  
3. Close the output stream once serialization is done.  
4. Create an `ObjectInputStream` and read the object back from the file.  
5. Cast the retrieved object to its original class and access its data.



## PROGRAM:
#### Developed By: Visalan H
#### Register Number: 212223240183

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

Program executed executed successfully.
