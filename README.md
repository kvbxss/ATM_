# ATM_


# What it is?

This is a Java Program to Display the ATM Transaction.
The user will choose from any one of the available options as input. 
Different cases using switch case have been provided for different operations like withdraw, deposit and check balance.
Here is the source code of the Java Program to Display the ATM Transaction.
The Java program is successfully compiled and run on a Windows system. 

```
package com.company;
import java.util.Scanner;
class ATM_Transaction
{
    public static void main(String args[] )
    {
        int balance = 5000, withdraw, deposit;
        Scanner s = new Scanner(System.in);
        while(true)
        {
            System.out.println("Automated Teller Machine");
            System.out.println("Choose 1 for Withdraw");
            System.out.println("Choose 2 for Deposit");
            System.out.println("Choose 3 for Check Balance");
            System.out.println("Choose 4 for EXIT");
            System.out.print("Choose the operation you want to perform:");
            int n = s.nextInt();
            switch(n)
            {
                case 1:
                    System.out.print("Enter money to be withdrawn:");
                    withdraw = s.nextInt();
                    if(balance >= withdraw)
                    {
                        balance = balance - withdraw;
                        System.out.println("Please collect your money");
                    }
                    else
                    {
                        System.out.println("Insufficient Balance");
                    }
                    System.out.println("");
                    break;

                case 2:
                    System.out.print("Enter money to be deposited:");
                    deposit = s.nextInt();
                    balance = balance + deposit;
                    System.out.println("Your Money has been successfully depsited");
                    System.out.println("");
                    break;

                case 3:
                    System.out.println("Balance : "+balance);
                    System.out.println("");
                    break;

                case 4:
                    System.exit(0);
            }
        }
    }
}


```

The program output is also shown below.

```
$ javac ATM_Transaction.java
$ java ATM_Transaction
 
Automated Teller Machine
Choose 1 for Withdraw
Choose 2 for Deposit
Choose 3 for Check Balance
Choose 4 for EXIT
Choose the operation you want to perform:1
Enter money to be withdrawn:2000
Please collect your money
 
Automated Teller Machine
Choose 1 for Withdraw
Choose 2 for Deposit
Choose 3 for Check Balance
Choose 4 for EXIT
Choose the operation you want to perform:3
Balance : 3000
 
Automated Teller Machine
Choose 1 for Withdraw
Choose 2 for Deposit
Choose 3 for Check Balance
Choose 4 for EXIT
Choose the operation you want to perform:4
```
