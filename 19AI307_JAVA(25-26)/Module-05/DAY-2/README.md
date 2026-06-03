# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:
Write a Java program to demonstrate **Serialization and Deserialization** of objects.


## AIM:
To write a Java program to demonstrate **object serialization and deserialization using ObjectOutputStream and ObjectInputStream**.

## ALGORITHM :
1. Start the program.  
2. Import the necessary packages `java.io` and `java.util`.  
3. Create a class `Student` that implements `Serializable`.  
4. Declare variables `id`, `name`, and `marks`.  
5. Create a constructor to initialize values.  
6. Override `toString()` method to display student details.  
7. Create a method `serializeStudents()` to write objects into a file.  
8. Use `ObjectOutputStream` with `FileOutputStream`.  
9. Create a method `deserializeStudents()` to read objects from a file.  
10. Use `ObjectInputStream` with `FileInputStream`.  
11. In the main method, read student details from the user.  
12. Store student objects in a list.  
13. Serialize the list into a file.  
14. Deserialize the list from the file.  
15. Display the deserialized student details.  
16. Stop the program.


## PROGRAM:

```java
/*
Program to implement Serialization and Deserialization using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/

import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine();

        for(int i = 0; i < n; i++){
            int id = scanner.nextInt();
            String name = scanner.next();
            double marks = scanner.nextDouble();

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

---

## SOURCE CODE:

Compile the program using

```
javac StudentSerializationUserInput.java
```

Run the program using

```
java StudentSerializationUserInput
```

---

## OUTPUT:

<img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/f4b54655-e9b3-468b-94bc-da48f74fdd65" />


---

## RESULT:

Thus, the Java program to demonstrate **Serialization and Deserialization** was executed successfully and the output was verified.
