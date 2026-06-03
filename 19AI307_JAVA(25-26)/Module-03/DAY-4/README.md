# Ex.No:3(D) INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.
AggressiveController: Allows only if "GREEN".
DefensiveController: Allows for "GREEN" or "YELLOW".

## AIM:
To develop a Java program that decides whether a vehicle can move or must stop based on the signal color and the type of traffic controller (Aggressive or Defensive) using interfaces.

## ALGORITHM :
1. Define an interface `TrafficController` with the method:
   - `boolean canGo(String signalColor)`
2. Create class `AggressiveController` implementing the interface:
   - Allows passage only if the signal color is GREEN.
3. Create class `DefensiveController` implementing the interface:
   - Allows passage if the signal color is GREEN or YELLOW.
4. In the `main` method:
   - Read `color` (signal color)
   - Read `type` (controller type: 1 or 2)
5. Based on `type`:
   - If 1 → create `AggressiveController`
   - Else → create `DefensiveController`
6. Call `canGo(color)` to check permission.
7. If true → print `"GO"`
   - Else → print `"STOP"`
8. End the program.

## PROGRAM:
  ```
/*
Program to implement a conditional statement using Java
Developed by: KARUNIYA M
RegisterNumber:  212223240068
*/
```

## SOURCE CODE:
```
import java.util.*;

interface TrafficController {
    boolean canGo(String signalColor);
}

class AggressiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN");
    }
}

class DefensiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String color = sc.next();
        int type = sc.nextInt();

        TrafficController ctrl = (type == 1) ? new AggressiveController() : new DefensiveController();

        if (ctrl.canGo(color))
            System.out.println("GO");
        else
            System.out.println("STOP");
    }
}
```

## OUTPUT:
<img width="431" height="202" alt="image" src="https://github.com/user-attachments/assets/893c86c5-b2f8-4240-8d2b-98ca05b093a6" />

## RESULT:
The program successfully determines whether a vehicle can move based on the signal color and controller type using interface-based polymorphism.


