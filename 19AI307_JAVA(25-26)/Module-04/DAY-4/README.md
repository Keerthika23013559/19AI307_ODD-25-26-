# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Write a Java program to implement the **Abstract Factory Design Pattern** to create UI components (Button and Checkbox) for different themes.

---

## AIM:
To write a Java program to demonstrate the **Abstract Factory Design Pattern** by creating related objects without specifying their concrete classes.

---

## ALGORITHM :
1. Start the program.  
2. Import the necessary package `java.util`.  
3. Create interfaces `Button` and `Checkbox` with method `render()`.  
4. Create concrete classes `DarkButton`, `LightButton`, `DarkCheckbox`, and `LightCheckbox`.  
5. Implement the `render()` method in each class.  
6. Create an interface `UIFactory` with methods `createButton()` and `createCheckbox()`.  
7. Create concrete factory classes `DarkThemeFactory` and `LightThemeFactory`.  
8. Implement factory methods to return corresponding objects.  
9. In the main class, read the theme input from the user.  
10. Based on input, create the appropriate factory object.  
11. Use the factory to create UI components.  
12. Call the `render()` methods to display output.  
13. Stop the program.

---

## PROGRAM:

```java
/*
Program to implement Abstract Factory Pattern using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/

import java.util.Scanner;

interface Button { void render(); }
interface Checkbox { void render(); }

// Concrete Button classes
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

// Concrete Checkbox classes
class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

// Abstract Factory
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Concrete Factories
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String theme = scanner.nextLine().toLowerCase();

        UIFactory factory;

        if (theme.equals("dark"))
            factory = new DarkThemeFactory();
        else if (theme.equals("light"))
            factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().render();
        factory.createCheckbox().render();
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


<img width="545" height="266" alt="image" src="https://github.com/user-attachments/assets/00ef4853-0c0d-4b06-af77-d3d09101d1aa" />

---

## RESULT:

Thus, the Java program to implement the **Abstract Factory Design Pattern** was executed successfully and the output was verified.
