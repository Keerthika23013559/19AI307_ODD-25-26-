# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to demonstrate **thread priority**.


## AIM:
To write a Java program to demonstrate **setting and displaying thread priorities**.


## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Main`.  
4. Inside the `main()` method create a `Scanner` object.  
5. Read two thread names from the user.  
6. Create two thread objects `t1` and `t2`.  
7. Set the names of the threads using `setName()`.  
8. Assign priorities using `setPriority()`.  
9. Display thread details using `System.out.println()`.  
10. Stop the program.


## PROGRAM:

```java
/*
Program to implement Thread Priority using Java
Developed by: KEERTHIKA M P
RegisterNumber:  212223240071
*/

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        
        t1.setName(name1);
        t2.setName(name2);
        
        t1.setPriority(4);
        t2.setPriority(2);
        
        System.out.println(t1);
        System.out.println(t2);
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


## OUTPUT:

<img width="698" height="212" alt="image" src="https://github.com/user-attachments/assets/a2e9cb3f-7ab1-4769-8998-8516070364e0" />



## RESULT:

Thus, the Java program to demonstrate **thread priority** was executed successfully and the output was verified.
