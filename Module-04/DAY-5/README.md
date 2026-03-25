# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Simulate a fan speed controller using the State Pattern. Each time the user types "next", change fan speed from Off -> Low -> Medium -> High -> Off.


<img width="313" height="188" alt="image" src="https://github.com/user-attachments/assets/2b6481db-82bd-4512-b8ba-ac0a3734e6ea" />



## AIM:

To simulate a fan speed controller using the State Pattern, where each press of "next" changes the fan speed in the sequence: Off → Low → Medium → High → Off.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a FanState interface with methods handleRequest() and getStateName().
4.	Implement concrete states: OffState, LowState, MediumState, and HighState. Each state changes to the next when handleRequest() is called
5.	Create a FanContext class that maintains the current state of the fan.
6.	On each "next" input from the user, call pressButton() to transition to the next state and display the current fan speed.
7.	Exit the program when the user types "exit".

   


## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: JESLIN GNANAWSHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

// State interface
interface FanState {
    void handleRequest(FanContext ctx);
    String getStateName();
}

// Concrete States
class OffState implements FanState {
    public void handleRequest(FanContext ctx) {
        ctx.setState(new LowState());
        System.out.println("Fan is on Low");
    }
    public String getStateName() {
        return "Off";
    }
}

class LowState implements FanState {
    public void handleRequest(FanContext ctx) {
        ctx.setState(new MediumState());
        System.out.println("Fan is on Medium");
    }
    public String getStateName() {
        return "Low";
    }
}

class MediumState implements FanState {
    public void handleRequest(FanContext ctx) {
        ctx.setState(new HighState());
        System.out.println("Fan is on High");
    }
    public String getStateName() {
        return "Medium";
    }
}

class HighState implements FanState {
    public void handleRequest(FanContext ctx) {
        ctx.setState(new OffState());
        System.out.println("Fan is Off");
    }
    public String getStateName() {
        return "High";
    }
}

// Context
class FanContext {
    private FanState state;

    public FanContext() {
        state = new OffState();
    }

    public void setState(FanState state) {
        this.state = state;
    }

    public void pressButton() {
        state.handleRequest(this);
    }
}

public class FanSpeedController {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        FanContext fan = new FanContext();
        String input;

        while (true) {
            input = sc.nextLine();

            if (input.equalsIgnoreCase("next")) {
                fan.pressButton();
            } else if (input.equalsIgnoreCase("exit")) {
                break;
            }
        }
        sc.close();
    }
}

```



## OUTPUT:

<img width="679" height="583" alt="image" src="https://github.com/user-attachments/assets/38f8ce1b-222f-4e1a-ae32-d6581d76e30e" />



## RESULT:

Thus, the program successfully cycles the fan speed through Off → Low → Medium → High → Off each time "next" is entered, demonstrating the State Pattern in action.


