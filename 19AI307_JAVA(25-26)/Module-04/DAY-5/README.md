# Ex.No:4(E) DESIGN PATTERN ---- BEHAVIOUR PATTERN

## QUESTION:
Write a Java program to demonstrate a **Behavioral Design Pattern** using the **Observer Pattern**.

---

## AIM:
To write a Java program to demonstrate the **Observer Pattern**, where multiple objects are notified when a change occurs.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create an interface `Observer` with a method `update()`.  
4. Create a class `Subscriber` that implements the `Observer` interface.  
5. Define a variable `name` and override the `update()` method.  
6. Create a class `Channel` (Subject).  
7. Declare a list to store observers (subscribers).  
8. Create a method `subscribe()` to add observers.  
9. Create a method `notifySubscribers()` to notify all observers.  
10. Create a method `uploadVideo()` to simulate a change and notify observers.  
11. In the main class, create a `Channel` object.  
12. Read subscriber details and add them to the channel.  
13. Read video title and call `uploadVideo()`.  
14. Display notifications for each subscriber.  
15. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement Behaviour Pattern using Java (Observer Pattern)
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/

import java.util.*;

interface Observer {
    void update(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    public void update(String channelName, String videoTitle) {
        System.out.println(name + " received notification: " + channelName + " uploaded " + videoTitle);
    }
}

class Channel {
    private String channelName;
    private List<Observer> subscribers = new ArrayList<>();

    public Channel(String name) {
        this.channelName = name;
    }

    public void subscribe(Observer o) {
        subscribers.add(o);
    }

    public void notifySubscribers(String videoTitle) {
        for (Observer o : subscribers) {
            o.update(channelName, videoTitle);
        }
    }

    public void uploadVideo(String videoTitle) {
        System.out.println(channelName + " uploaded: " + videoTitle);
        notifySubscribers(videoTitle);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String channelName = sc.nextLine();
        Channel channel = new Channel(channelName);

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            channel.subscribe(new Subscriber(name));
        }

        String videoTitle = sc.nextLine();
        channel.uploadVideo(videoTitle);
    }
}
```

---

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
TechWorld
2
Hari
Priya
Java Basics
TechWorld uploaded: Java Basics
Hari received notification: TechWorld uploaded Java Basics
Priya received notification: TechWorld uploaded Java Basics
```

---

## RESULT:

Thus, the Java program to demonstrate the **Behavioral Design Pattern (Observer Pattern)** was executed successfully and the output was verified.
