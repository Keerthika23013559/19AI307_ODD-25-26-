# Ex.No:5(C) FILE HANDLING USING JAVA

## QUESTION:
Write a Java program to perform **file handling operations** and count the number of words in a file.


## AIM:
To write a Java program to demonstrate **file handling using FileWriter and BufferedReader** and count the number of words in a file.


## ALGORITHM :
1. Start the program.  
2. Import the necessary packages `java.io` and `java.util`.  
3. Create a class `Main`.  
4. Inside the `main()` method create a `Scanner` object.  
5. Read a string input from the user.  
6. Create a `FileWriter` object and write the input into a file (`sample.txt`).  
7. Close the file after writing.  
8. Open the file using `FileReader` and wrap it with `BufferedReader`.  
9. Initialize a variable `count` to 0.  
10. Read the file line by line using `readLine()`.  
11. Split each line into words using `split(" ")`.  
12. Count the number of words and store in `count`.  
13. Close the file after reading.  
14. Display the total number of words.  
15. Stop the program.


## PROGRAM:

```java
/*
Program to implement File Handling using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/

import java.io.*;
import java.util.Scanner;

public class Main{
    public static void main(String[] args) throws Exception{

        Scanner sc = new Scanner(System.in);

        String text = sc.nextLine();
        
        FileWriter fw = new FileWriter("sample.txt");
        fw.write(text);
        fw.close();
        
        BufferedReader br = new BufferedReader(new FileReader("sample.txt"));

        int count = 0;
        
        while((text = br.readLine()) != null){
            String[] words = text.split(" ");
            count += words.length;
        }
        
        br.close();
        
        System.out.println("Number of words in the file: " + count);
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

<img width="947" height="229" alt="image" src="https://github.com/user-attachments/assets/0d385bd9-50d5-495d-8614-7cc7159f88c1" />


---

## RESULT:

Thus, the Java program to demonstrate **file handling and word count using FileWriter and BufferedReader** was executed successfully and the output was verified.
