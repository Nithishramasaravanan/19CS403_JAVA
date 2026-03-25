# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

For example:

<img width="736" height="156" alt="image" src="https://github.com/user-attachments/assets/a7e5a0ba-23f2-43f2-a4a5-d9136b25cb0e" />


## AIM:

To create a Student class, set its details using a method, and display the name and roll number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a Student class with variables name and rollNumber.
4.	Create a method setDetails(String name, int rollNumber) to assign values.
5.	Create a method display() to print the student details.
6.	In the main method, read name and roll number from the user.
7.	Create a Student object, call setDetails() with input values, and then call display().
8.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```

import java.util.Scanner;

class Student {
    // Instance variables for name and roll number
    String name;
    int rollNumber;

    // Method to set details of the student
    void setDetails(String name, int rollNumber) {
        // Assigning the name and roll number to the instance
        this.name = name;  
        this.rollNumber = rollNumber;   variable
    }

    // Method to display the student's details
    void display() {
        System.out.println("Name: " + name);
        System.out.println("Roll Number: " + rollNumber);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Student student = new Student();

        String name = sc.nextLine();  
        

        int rollNumber = sc.nextInt();

        student.setDetails(name, rollNumber);

        student.display();

        sc.close();
    }
}
```





## OUTPUT:

<img width="755" height="477" alt="image" src="https://github.com/user-attachments/assets/c7f21cb5-5f25-4142-b58e-86e82d92c67f" />


## RESULT:

The program successfully sets and displays the student’s name and roll number.
