# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

 
For example:

<img width="601" height="194" alt="image" src="https://github.com/user-attachments/assets/3316a829-bbc6-40f6-aa7e-710b33533147" />


## AIM:
To write a Java program that reads multiple lines of input and prints only the lines containing the word "Java".

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Initialize a list to store lines containing "Java".
4.	Read lines continuously until "exit" is entered.
5.	Check if each line contains "Java".
6.	If it does, add it to the list.
7.	After reading all lines, print the lines stored in the list.
8.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:



```
import java.util.ArrayList;
import java.util.Scanner;

public class PrintJavaLines {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<String> matchingLines = new ArrayList<>();

        String line;
        
        // Read input lines until "exit"
        while (!(line = sc.nextLine()).equals("exit")) {
            if (line.contains("Java")) {
                matchingLines.add(line);
            }
        }

        // Print results
        System.out.println("Lines containing the word 'Java':");
        for (String s : matchingLines) {
            System.out.println(s);
        }

        sc.close();
    }
}

```



## OUTPUT:

<img width="1149" height="490" alt="image" src="https://github.com/user-attachments/assets/19d1038d-e34e-4086-bf26-576b0659a479" />


## RESULT:

The program successfully reads multiple lines and prints only the lines containing "Java".

