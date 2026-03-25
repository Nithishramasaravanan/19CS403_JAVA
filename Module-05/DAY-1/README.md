# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 
<img width="618" height="155" alt="image" src="https://github.com/user-attachments/assets/f0644a2c-0662-4ea0-af6b-25edda50bb3d" />

## AIM:
To write a Java program that reads user input from the keyboard using InputStreamReader and displays a greeting message.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an InputStreamReader object connected to System.in.
4.	Wrap it with a BufferedReader to read text easily.
5.	Read a line of input (user name).
6.	Display the greeting message: "Hello, <name>!".
7.	End the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```
import java.io.InputStreamReader;
import java.io.BufferedReader;
import java.io.IOException;

public class ReadInputStreamReader {
    public static void main(String[] args) {
        // Create InputStreamReader object linked to System.in
        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);


        try {
            String name = br.readLine(); // Read input from user
            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            System.out.println("Error reading input: " + e.getMessage());
        }
    }
}
```




## OUTPUT:

<img width="661" height="302" alt="image" src="https://github.com/user-attachments/assets/c9e209e4-2a90-4351-86c0-fde2581890ce" />


## RESULT:
Thus, the program successfully reads user input using InputStreamReader and prints the greeting message.
