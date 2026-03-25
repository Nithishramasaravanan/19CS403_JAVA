# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables
```
import java.util.Scanner;

 class Rectangle {
    // Private instance variables
    private double length;
    private double width;

    // Getter and Setter for length
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }

    // Getter and Setter for width
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }

    // Method to calculate area
    public double calculateArea() {
        return length * width;
    }
}
```

## AIM:

To create a Rectangle class with private variables and access them using public getter and setter methods.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a class Rectangle with private instance variables length and width.
4.	Provide public getter and setter methods for both variables.
5.	In the main method, create a Rectangle object.
6.	Read length and width from the user and set them using setter methods.
7.	Display the length and width.
8.	Stop the program.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```

import java.util.Scanner;

class Rectangle {
    // Private instance variables
    private double length;
    private double width;

    // Getter and Setter for length
    public double getLength() {
        return length;
    }

    public void setLength(double length) {
        this.length = length;
    }

    // Getter and Setter for width
    public double getWidth() {
        return width;
    }

    public void setWidth(double width) {
        this.width = width;
    }

    // Method to calculate the area
    public double calculateArea() {
        return length * width;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Create a Rectangle object
        Rectangle rectangle = new Rectangle();

        // input length
        double length = scanner.nextDouble();
        rectangle.setLength(length);  

        // input width
        double width = scanner.nextDouble();
        rectangle.setWidth(width);  

      System.out.println("Length: "+length);
      System.out.println("Width: "+width);

        scanner.close();
    }
}


```

## OUTPUT:
<img width="700" height="515" alt="image" src="https://github.com/user-attachments/assets/e3d144c7-a00f-42b5-8bda-91bb6e6cea9f" />



## RESULT:

The program correctly sets and retrieves the rectangle’s length and width using getter and setter methods.
