# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to demonstrate the concept of **Inner Class**.


## AIM:
To write a Java program to demonstrate the **Inner Class concept by accessing inner class methods from outer class**.


## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `OuterClass`.  
4. Inside it, create an inner class `InnerClass`.  
5. Define a method `display()` in the inner class to print a message.  
6. In the outer class, create a method `accessInner()` to create an object of the inner class.  
7. Call the inner class method using the object.  
8. In the `main()` method, create a `Scanner` object.  
9. Read the name from the user.  
10. Create an object of `OuterClass`.  
11. Call the method to access the inner class.  
12. Display the output.  
13. Stop the program.


## PROGRAM:

```java
/*
Program to implement Inner Class using Java
Developed by: KARUNIYA M
RegisterNumber: 212223240068
*/

import java.util.Scanner;

class OuterClass{

    class InnerClass{
        public void display(String name){
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public void accessInner(String name){
        InnerClass inner = new InnerClass();
        inner.display(name);
    }
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine().trim();

        OuterClass outer = new OuterClass();
        outer.accessInner(name);
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

<img width="1015" height="227" alt="image" src="https://github.com/user-attachments/assets/83606ba7-2c05-4889-8c55-ea8e341e93d8" />



## RESULT:

Thus, the Java program to demonstrate the **Inner Class concept** was executed successfully and the output was verified.
