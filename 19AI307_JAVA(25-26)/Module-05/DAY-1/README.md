# Ex.No:5(A) INPUTSTREAMREADER 


## AIM:
Read character data from a byte-based input stream.

## ALGORITHM :
1.	Start by creating a byte-based input stream (e.g., `System.in`).  
2. Wrap it inside an `InputStreamReader` to translate bytes into characters.  
3. Prompt the user for input and begin reading characters using `read()`.  
4. Continue reading until the stream ends or a stopping condition is met.  
5. Close the reader to free system resources.



## PROGRAM:
#### Program to implement a InputStreamReader using Java
## SOURCE CODE:

import java.io.*;

public class InputStreamReaderExample {
    public static void main(String[] args) {
        try {
            // Byte-based input (keyboard)
            InputStream inputStream = System.in;

            // Convert bytes to characters
            InputStreamReader reader = new InputStreamReader(inputStream);

            System.out.println("Type something and press Enter:");

            int data = reader.read();
            while (data != -1) {
                char ch = (char) data;
                System.out.print(ch);
                if (ch == '\n') break; // stop after new line
                data = reader.read();
            }

            reader.close();
        } catch (IOException e) {
            System.out.println("Oops! Something went wrong: " + e.getMessage());
        }
    }
}

## OUTPUT:



## RESULT:
