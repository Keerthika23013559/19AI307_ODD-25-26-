# Ex.No:5(A) INPUTSTREAMREADER

## QUESTION:
Write a Java program to read input from the user using **InputStreamReader**.



## AIM:
To write a Java program to demonstrate **reading input using InputStreamReader and BufferedReader**.



## ALGORITHM :
1. Start the program.  
2. Import the necessary packages `java.io`.  
3. Create a class `Main`.  
4. Inside the `main()` method create an object of `InputStreamReader`.  
5. Wrap it using `BufferedReader` to read input efficiently.  
6. Read a string input using `readLine()`.  
7. Display the entered input.  
8. Handle exceptions using `throws IOException`.  
9. Stop the program.



## PROGRAM:

```java
/*
Program to implement InputStreamReader using Java
Developed by: KEERTHIKA M P
RegisterNumber:  212223240071
*/

import java.io.*;

public class Main{
    public static void main(String[] args) throws IOException{

        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);

        String input = br.readLine();

        System.out.println("You entered: " + input);
    }
}
```


## SOURCE CODE:

Compile the program using

```
javac Main.java
```

Run the program using

```
java Main
```

---

## OUTPUT:

```
Hello Java
You entered: Hello Java
```


## RESULT:

Thus, the Java program to read input using **InputStreamReader and BufferedReader** was executed successfully and the output was verified.
