# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.

For example:

<img width="253" height="257" alt="image" src="https://github.com/user-attachments/assets/90e8704d-9934-405b-9675-a795b319ea09" />





## AIM:
To write a Java program that creates two threads to print "Hello" and "World" alternately using synchronized blocks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read n — number of times to print.
4. Create a shared lock object and a boolean flag to control turns.
5.	Create Thread 1 to print "Hello" when it's its turn.
6.	Create Thread 2 to print "World" when it's its turn.
7.	Use synchronized, wait(), and notify() to alternate printing.
8.	Start both threads.
9.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class HelloWorldSimple {

    private static final Object lock = new Object();
    private static boolean helloTurn = true; // Hello prints first

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        Thread helloThread = new Thread(() -> {
            for (int i = 0; i < n; i++) {
                synchronized (lock) {
                    while (!helloTurn) {
                        try { lock.wait(); } catch (Exception e) {}
                    }
                    System.out.println("Hello");
                    helloTurn = false;
                    lock.notify();
                }
            }
        });

        Thread worldThread = new Thread(() -> {
            for (int i = 0; i < n; i++) {
                synchronized (lock) {
                    while (helloTurn) {
                        try { lock.wait(); } catch (Exception e) {}
                    }
                    System.out.println("World");
                    helloTurn = true;
                    lock.notify();
                }
            }
        });

        helloThread.start();
        worldThread.start();
    }
}

```





## OUTPUT:

<img width="578" height="864" alt="image" src="https://github.com/user-attachments/assets/e303add0-d38e-4c42-866d-766651114e44" />



## RESULT:
Thus, the program successfully prints "Hello" and "World" alternately using two threads and synchronized blocks.


