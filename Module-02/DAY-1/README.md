# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.

When staticMethod() is called, it should print  "I am static".

When nonStaticMethod() is called, it should print  "I am non-static"

For example:
<img width="485" height="163" alt="image" src="https://github.com/user-attachments/assets/bc088df5-b893-4c9f-8d24-3a7d706a7957" />


## AIM:

To write a Java program that demonstrates calling a static method and a non-static method from the main method.

## ALGORITHM :
1.	Start the program.
2.	Create a class containing one static method and one non-static method.
3.	In the static method, print “I am static”.
4.	In the non-static method, print “I am non-static”.
5.	From the main method, call the static method directly.
6.	Create an object and call the non-static method.
7.	Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```
public class MyClass {

    // Static method
    public static void staticMethod() {
        System.out.println("I am static");
    }

    // Non-static method
    public void nonStaticMethod() {
        System.out.println("I am non-static");
    }

    public static void main(String[] args) {
        // Call the static method directly using the class name

        MyClass.staticMethod();
        
        // Create an object to call the non-static method

        MyClass obj = new MyClass();
        obj.nonStaticMethod();
    }
}

```



## OUTPUT:

<img width="676" height="325" alt="image" src="https://github.com/user-attachments/assets/62b4a340-cdea-4381-926f-ded08d4617a5" />


## RESULT:

The program successfully calls both static and non-static methods and displays the expected output.
