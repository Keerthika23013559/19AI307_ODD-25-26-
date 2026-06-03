# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()


## AIM:
To create an Employee class where the display() method returns the current object using this, and demonstrate calling display().printName() from another method.

## ALGORITHM :
1. Create a class Employee with a variable name.

2. Write a method setName() to assign value to name.

3. Write a method display() that returns the current object using return this;.

4. Write a method printName() to print the employee name.

5. Add another method show() that internally calls display().printName().

6. In the main() method, read the employee name from the user.

7.Create an Employee object and set the name.

8. Call both display().printName() and show() to demonstrate method chaining.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Employee {
    String name;

    void setName(String name) {
        this.name = name;  
    }

    Employee display() {
        return this;  
    }

    void printName() {
        System.out.println("Employee Name: " + name);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String inputName = scanner.nextLine();

        Employee emp = new Employee();
        emp.setName(inputName);
        emp.display().printName();  
    }
}
```


## OUTPUT:

<img width="686" height="326" alt="image" src="https://github.com/user-attachments/assets/954fafa4-a638-4044-b666-3322017194cd" />


## RESULT:
Therefore the program successfully returns the current object using this inside the display() method.



