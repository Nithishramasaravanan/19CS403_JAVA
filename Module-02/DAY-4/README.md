# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Demonstrate variable shadowing by declaring an instance variable and a local variable with the same name inside a method. Print both values.
<img width="655" height="200" alt="image" src="https://github.com/user-attachments/assets/bff65272-d330-4a94-823b-3d3323c4eb79" />


## AIM:
To demonstrate variable shadowing by showing the difference between a local variable and an instance variable with the same name.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Declare an instance variable number.
4.	Create a method that takes a parameter with the same name number.
5.	Inside the method, print the local variable (number) and instance variable (this.number).
6.	In the main method, read input from the user.
7.	Create an object of the class and call the method, passing the input.
8.	Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

public class VariableShadowingExample {

    int number = 10; // Instance variable

    public void showNumber(int number) { 
        System.out.println("Local variable number: " + number);   // Local variable
        System.out.println("Instance variable number: " + this.number); // Instance variable
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int input = sc.nextInt(); // Read input for local variable
        VariableShadowingExample obj = new VariableShadowingExample();
        obj.showNumber(input);

        sc.close();
    }
}


```

## OUTPUT:

<img width="857" height="469" alt="image" src="https://github.com/user-attachments/assets/184f6340-39fe-4121-b55c-fb06dbb4e49f" />


## RESULT:
The program successfully demonstrates variable shadowing by printing both local and instance variable values.

