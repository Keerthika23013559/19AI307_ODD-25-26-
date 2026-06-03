# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that defines a class BankAccount with private attributes accountNumber and balance, and provides public getter and setter methods to access and modify these values.

## ALGORITHM :
1. Define a class BankAccount with two private instance variables:

        String accountNumber

        double balance

3. Create public getter and setter methods for both variables:

      getAccountNumber() and setAccountNumber()
   
   
      getBalance() and setBalance()

5. In the main() method, create a Scanner object to read input from the user.

6. Create an object of the BankAccount class.

7. Read the account number and balance from the user and store them using setter methods.

8. Retrieve and print the stored values using getter methods.

9. Close the Scanner and end the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class BankAccount {
   
    private String accountNumber;
    private double balance;

    
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

   
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        BankAccount account = new BankAccount();

        String accNo = sc.nextLine();
        double bal = sc.nextDouble();

        account.setAccountNumber(accNo);
        account.setBalance(bal);

        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Balance: " + account.getBalance());

        sc.close();
    }
}
```

## OUTPUT:
<img width="826" height="465" alt="image" src="https://github.com/user-attachments/assets/972c4fcf-d9d0-43f8-bc30-518764a4d55e" />



## RESULT:
Therfore the program successfully stores account details using setter methods and retrieves them using getter methods.




