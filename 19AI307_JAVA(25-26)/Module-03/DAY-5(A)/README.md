# Ex.No:5(E) MULTITHREADING - SYNCHRONIZATION

## QUESTION:
Write a Java program to demonstrate **multithreading with synchronization** using `wait()` and `notify()`.


## AIM:
To write a Java program to demonstrate **thread synchronization** using `synchronized`, `wait()`, and `notify()` methods.
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
Developed by: KEERTHIKA M P
RegisterNumber: 212223240071
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


## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create a class `Printer`.  
4. Declare a boolean variable `helloTurn` to control execution.  
5. Create a synchronized method `printHello()`:
   - Wait if it is not hello’s turn.  
   - Print "Hello".  
   - Change turn and notify the other thread.  
6. Create another synchronized method `printWorld()`:
   - Wait if it is not world’s turn.  
   - Print "World".  
   - Change turn and notify the other thread.  
7. Create a class `HelloThread` extending `Thread`.  
8. Override `run()` to call `printHello()` `n` times.  
9. Create a class `WorldThread` extending `Thread`.  
10. Override `run()` to call `printWorld()` `n` times.  
11. In the main class, read integer `n` from the user.  
12. Create a `Printer` object.  
13. Create two threads (`HelloThread` and `WorldThread`).  
14. Start both threads.  
15. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement Multithreading Synchronization using Java
Developed by: KEERTHIKA M P
RegisterNumber: 212223240071
*/

import java.util.*;

class Printer {
    private boolean helloTurn = true;

    public synchronized void printHello() {
        try {
            while (!helloTurn)
                wait();

            System.out.println("Hello");
            helloTurn = false;
            notify();
        } catch (Exception e) {}
    }

    public synchronized void printWorld() {
        try {
            while (helloTurn)
                wait();

            System.out.println("World");
            helloTurn = true;
            notify();
        } catch (Exception e) {}
    }
}

class HelloThread extends Thread {
    Printer p;
    int n;

    HelloThread(Printer p, int n) {
        this.p = p;
        this.n = n;
    }

    public void run() {
        for (int i = 0; i < n; i++)
            p.printHello();
    }
}

class WorldThread extends Thread {
    Printer p;
    int n;

    WorldThread(Printer p, int n) {
        this.p = p;
        this.n = n;
    }

    public void run() {
        for (int i = 0; i < n; i++)
            p.printWorld();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        Printer p = new Printer();

        Thread t1 = new HelloThread(p, n);
        Thread t2 = new WorldThread(p, n);

        t1.start();
        t2.start();
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

<img width="200" height="600" alt="image" src="https://github.com/user-attachments/assets/cc2834aa-43bb-45ce-99f3-2966b164c933" />



## RESULT:

Thus, the Java program to demonstrate **multithreading with synchronization using wait() and notify()** was executed successfully and the output was verified.
