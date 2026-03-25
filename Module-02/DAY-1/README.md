# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

```
import java.util.Scanner;
class City {

    String cityName;
    long population;
    double area;

    void printDetails() {
           // Your Code Here
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
         // Your Code Here
         scanner.close();
    }
}
```


For example:


<img width="450" height="304" alt="image" src="https://github.com/user-attachments/assets/b207f2f2-3220-4eda-8983-0d7051c22eff" />


## AIM:

To write a Java program that creates a City class, stores its details using an object, and prints all the attributes

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a class City with attributes: cityName, population, and area.
4.	Define a method printDetails() to display the city information.
5.	In the main method, read the city details as input from the user.
6.	Create an object of the City class and assign the input values.
7.	Call the printDetails() method to display the details.
8.	Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class City {

    String cityName;
    long population;
    double area;

    // Method to print the details of the city
    void printDetails() {
        System.out.println("City Name: " + cityName);
        System.out.println("Population: " + population);
        System.out.println("Area: " + area);
    }
}

public class Prog {  // Change class name from 'prog' to 'Prog'
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // new City object
        City city = new City();

        //  input for city name, population, and area
        city.cityName = scanner.nextLine(); 
        city.population = scanner.nextLong(); 
        city.area = scanner.nextDouble(); 

        // Print the details of the city
        city.printDetails();

        scanner.close();
    }
}


```



## OUTPUT:

<img width="845" height="537" alt="image" src="https://github.com/user-attachments/assets/125cab94-5509-4759-86d3-df3ba52bf316" />


## RESULT:

The program successfully creates a City object and prints all its details.


