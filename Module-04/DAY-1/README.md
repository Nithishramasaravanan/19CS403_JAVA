# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that safely prints the value of an Integer object by checking for null and preventing a NullPointerException when .toString() is called.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input.
4.	Read an integer value from the user.
5.	Assign it to an Integer object.
6.	Check if the Integer object is null.
7.	If it is null, print "Null Integer".
8.	Otherwise, safely call .toString() and print the value.
9.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:


```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        
        try
        {
            Integer s=sc.nextInt();
            if(s==null || s==0){
                throw new NullPointerException();
            }
            else{
                System.out.println(s.toString());
            }
        }
        catch(Exception e)
        {
            System.out.println("Null Integer");
        }
    }
}
```




## OUTPUT:

<img width="809" height="495" alt="image" src="https://github.com/user-attachments/assets/331a1ed0-e410-4d66-98e8-f89b9a05dbef" />



## RESULT:

Thus, the program successfully checks for null before calling .toString() and prevents a NullPointerException.
