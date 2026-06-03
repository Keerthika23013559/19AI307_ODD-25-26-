# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a haunted house, lights turn on or off based on the hour of entry:

If the hour is even and between 2 and 6 (inclusive), lights flicker.

If the hour is odd and between 7 and 11, lights stay off.

If the hour is 12, lights turn red.

Otherwise, the house is dark.


## AIM:
To write a Java program that uses conditional statements to determine the state of lights in a haunted house based on the hour of entry.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.*.

3. Create a Scanner object to read the hour input from the user.

4. Read the hour as an integer.

5. Check if the hour is even and between 2 and 6 (inclusive):

6. Display “Lights flicker”.

7. Else if the hour is odd and between 7 and 11:

8. Display “Lights stay off”.

9. Else if the hour is 12:

10. Display “Lights turn red”.
 
11. Display “The house is dark”.

12. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/
```

## Sourcecode.java:
```
import java.util.*;
public class Demo
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
       if (a >= 2 && a <= 6 && a % 2 == 0) {
            System.out.println("Lights flicker");
        } else if (a>= 7 && a <= 11 && a % 2 != 0) {
            System.out.println("Lights off");
        } else if (a == 12) {
            System.out.println("Lights red");
        } else {
            System.out.println("Dark house");
        }
    }
}
```

## OUTPUT:
<img width="486" height="294" alt="Screenshot 2025-11-14 101547" src="https://github.com/user-attachments/assets/a64529b4-061c-436d-8ea4-55157b6e41b9" />





## RESULT:
Thus, the Java program to implement conditional statements for the haunted house lighting system was successfully executed.




