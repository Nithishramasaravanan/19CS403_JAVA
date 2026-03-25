# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the maximum odd number in an array

 
For example:

Input	Result
5
2
3
7
8
6
7
4
2
4
6
8
No odd number found


## AIM:
To write a Java program that reads an array of integers and finds the largest odd number in the array, displaying it or indicating if no odd number exists.

## ALGORITHM :
1. Start the program and create a Scanner object to read user input.

2. Read an integer value representing the size of the array.

3. Create an integer array of the given size.

4. Use a loop to read all array elements from the user and store them in the array.

5. Initialize a variable maxOdd with the minimum possible integer value.

6. Traverse the array and check each element; if it is odd and greater than maxOdd, update maxOdd.

7. After traversal, check if maxOdd is still the minimum value; if so, print "No odd number found".

8. Otherwise, print the largest odd number found.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber: 212222040062
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i = 0; i < n; i++){
            arr[i] = sc.nextInt();
        }
        int maxOdd = Integer.MIN_VALUE;
        for(int x : arr){
            if(x % 2 != 0 && x > maxOdd) maxOdd = x;
        }
        if(maxOdd == Integer.MIN_VALUE) System.out.println("No odd number found");
        else System.out.println(maxOdd);
    }
}
```


## OUTPUT:
<img width="536" height="577" alt="image" src="https://github.com/user-attachments/assets/a4eae550-318c-4961-9fef-866a62c4daf5" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
