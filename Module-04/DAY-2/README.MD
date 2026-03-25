# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Welcome to MatchIt – a dating app that automatically notifies users when their preferred type of match joins the platform.

Each user has their own preference:

Some are looking for "Gamers"

Some prefer "Pet Lovers"

Others vibe with "Bookworms"

Or maybe they're into "Gym Freaks", etc.

When a new user signs up, the app should only notify users whose preferences match that new person’s type.

Users subscribe to MatchIt’s notification service based on their “match interest”. The system notifies them only when someone with their preferred type signs up.

What Students Must Do:
Implement the Observer Pattern

MatchItServer = Subject

User = Observer

When a new person joins, notify only users who match the preference

Each user prints a custom message when their preferred type joins.

Input Format:
First line: Number of users n

Next n lines: UserName Preference
(e.g., Alice Gamer)

Next line: Number of sign-ups m

Next m lines: NewUserName Type
(e.g., Jack Gamer)

Output Format:
For each signup:

New User Joined: [NewUserName] - Type: [Type]
[UserName]: Omg! A new [Type]? MatchIt, you know me too well! 
...
Only matching users get notified.

For example:

<img width="973" height="443" alt="image" src="https://github.com/user-attachments/assets/a9eedc3f-78e5-4916-832d-6ef999d51c42" />



## AIM:
To write a Java program that implements the Observer Pattern where users get notified only when a new user joins with their preferred type.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Observer interface with methods notify() and getPreference().
4.	Create a User class that stores name and preference and prints a message when notified.
5.	Create a MatchItServer class to register users and notify only matching ones.
6.	Read number of users and their details; register them.
7.	Read number of new signups and notify only matching users.
8.	Display results.
9.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:

```
import java.util.*;

interface Observer {
    void notify(String name, String type);
    String getPreference();
}

class User implements Observer {
    private String userName;
    private String preference;

    public User(String userName, String preference) {
        this.userName = userName;
        this.preference = preference;
    }

    public String getPreference() {
        return preference;
    }

    public void notify(String name, String type) {
        System.out.println(userName + ": Omg! A new " + type + "? MatchIt, you know me too well! (It’s " + name + "!)");
    }
}

class MatchItServer {
    private List<Observer> observers = new ArrayList<>();

    public void register(Observer observer) {
        observers.add(observer);
    }

    public void newSignup(String newUserName, String type) {
        System.out.println("New User Joined: " + newUserName + " - Type: " + type);
        for (Observer observer : observers) {
            if (observer.getPreference().equalsIgnoreCase(type)) {
                observer.notify(newUserName, type);
            }
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MatchItServer server = new MatchItServer();

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] userInfo = sc.nextLine().split(" ");
            server.register(new User(userInfo[0], userInfo[1]));
        }

        int m = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < m; i++) {
            String[] newUser = sc.nextLine().split(" ");
            server.newSignup(newUser[0], newUser[1]);
        }

        sc.close();
    }
}

```





## OUTPUT:

<img width="1276" height="671" alt="image" src="https://github.com/user-attachments/assets/69a10eff-8f1c-4b0f-8986-49bd04be4d9d" />



## RESULT:
Thus, the program successfully implements the Observer Pattern and notifies only the matching users when a new user signs up.

