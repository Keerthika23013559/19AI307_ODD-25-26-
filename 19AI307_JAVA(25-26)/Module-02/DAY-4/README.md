# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a Java program that initializes object variables using a constructor and overrides the toString() method to display object details in a readable format.

## ALGORITHM :

1. Define a class Student with two instance variables:

     String name

     int age

2. Create a parameterized constructor to initialize these variables.

3. Override the toString() method to return the student details in a formatted string.

4. In the main() method:

    - Read the name and age from the user.

    - Create a Student object using the constructor.

5. Print the object, which automatically calls the overridden toString() method.

6. End the program.



## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Student {
    String name;
    int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class StudentDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name = scanner.nextLine();
        int age = scanner.nextInt();

        Student student = new Student(name, age);
        System.out.println(student.toString());
    }
}
```




## OUTPUT:
<img width="896" height="395" alt="image" src="https://github.com/user-attachments/assets/0b280b01-a09a-4749-b733-41411f01b00a" />




## RESULT:
Therefore the program successfully creates a student object using the constructor.



