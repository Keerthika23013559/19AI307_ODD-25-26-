# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.

## ALGORITHM :
1. Define a class demo with two methods:

     square(int n) → returns n * n.
     cube(int n) → returns n * square(n) by calling the square() method internally.

2. In the main class, read an integer input from the user.

3. Create an object of the demo class.

4. Call the cube() method using the object and print the result.

5. End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: KEERTHIKA M P
RegisterNumber:  212223240071
*/
```

## SOURCE CODE:
```
import java.util.*;
class demo
{
    public int square(int n)
    {
        return n*n;
    }
    public int cube(int n)
    {
        return n*square(n);
    }
    
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        demo d=new demo();
        System.out.println(d.cube(n));
    }
}
```


## OUTPUT:
<img width="392" height="243" alt="image" src="https://github.com/user-attachments/assets/aa929a40-c871-4a15-8d09-12604778a14b" />



## RESULT:
Therefore the program successfully computes the cube of a number by internally using the square method.



