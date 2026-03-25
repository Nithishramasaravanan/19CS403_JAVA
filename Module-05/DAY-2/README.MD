# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.
<img width="961" height="312" alt="image" src="https://github.com/user-attachments/assets/5f181cf3-5931-4ceb-a533-a7ddf5c3dc9d" />


## AIM:
To write a Java program that serializes a list of Student objects into a file and then deserializes them back to display the stored data.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read n (number of students).
4.	For each student, read id, name, and marks.
5.	Create Student objects and store them in an ArrayList.
6.	Serialize the ArrayList into a file using ObjectOutputStream.
7.	Deserialize the ArrayList from the file using ObjectInputStream.
8.	Display all deserialized student details.
9.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine(); // consume newline

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        // Serialize
        serializeStudents(students, fileName);

        // Deserialize
        List<Student> deserializedStudents = deserializeStudents(fileName);

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```



## OUTPUT:

<img width="1224" height="871" alt="image" src="https://github.com/user-attachments/assets/16eb0a33-f4fd-45ed-9c05-8531efb7f868" />


## RESULT:
Thus, the program successfully serializes a collection of Student objects into a file and deserializes them back for display.
