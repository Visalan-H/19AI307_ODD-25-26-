# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM

## AIM:

Design a sensor network using SOLID principles and the Observer pattern so that only relevant controllers react to Air Quality Index readings.

## ALGORITHM :

1. Start the program and read the number of AQI readings.
2. Create the subject (SensorNetwork) and register observers (controllers).
3. For each AQI reading, print the sensor report.
4. Notify only the observers whose AQI range matches the value.
5. Each reacting controller prints its action.

#### Developed By: Malar Mariam S

#### Register Number: 212223230118

## PROGRAM:

### to implement a SOLID Principles in Java Program

## SOURCE CODE:

```java
import java.util.*;

interface Observer {
    void update(String sensorId, int aqi);
}

interface Subject {
    void registerObserver(Observer o);
    void notifyObservers(String sensorId, int aqi);
}

class SensorNetwork implements Subject {
    private List<Observer> observers = new ArrayList<>();

    public void registerObserver(Observer o) {
        observers.add(o);
    }

    public void notifyObservers(String sensorId, int aqi) {
        for (Observer o : observers) {
            o.update(sensorId, aqi);
        }
    }
}

class GreenZoneController implements Observer {
    public void update(String sensorId, int aqi) {
        if (aqi < 100) {
            System.out.println("GreenZoneController: Taking appropriate action");
        }
    }
}

class AlertZoneController implements Observer {
    public void update(String sensorId, int aqi) {
        if (aqi >= 100 && aqi <= 200) {
            System.out.println("AlertZoneController: Taking appropriate action");
        }
    }
}

class DangerZoneController implements Observer {
    public void update(String sensorId, int aqi) {
        if (aqi > 200) {
            System.out.println("DangerZoneController: Taking appropriate action");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        SensorNetwork network = new SensorNetwork();

        network.registerObserver(new GreenZoneController());
        network.registerObserver(new AlertZoneController());
        network.registerObserver(new DangerZoneController());

        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String[] inp = sc.nextLine().split(" ");
            String sensorId = inp[0];
            int aqi = Integer.parseInt(inp[1]);

            System.out.println("Sensor " + sensorId + " reports AQI: " + aqi);
            network.notifyObservers(sensorId, aqi);
        }
    }
}
```

## OUTPUT:

```
Sensor S1 reports AQI: 85
GreenZoneController: Taking appropriate action
Sensor S2 reports AQI: 150
AlertZoneController: Taking appropriate action
Sensor S3 reports AQI: 250
DangerZoneController: Taking appropriate action
```

## RESULT:

Program executed successfully.
