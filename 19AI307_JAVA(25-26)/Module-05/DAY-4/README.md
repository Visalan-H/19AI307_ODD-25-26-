# Ex.No:5(D) THREAD PRIORITY

## QUESTION:


## AIM:
Demonstrate how thread priorities influence the order in which threads are scheduled.

## ALGORITHM :
1.	Create a thread class by extending `Thread` and override `run()`.  
2. Instantiate multiple thread objects.  
3. Assign different priorities using `setPriority()`.  
4. Start all threads using `start()`.  
5. Observe execution order influenced by assigned priorities.


#### Developed By: Visalan H
#### Register Number: 212223240183

## PROGRAM:

#### Program to implement a Thread Priority Concept using Java

## SOURCE CODE:
class PriorityThread extends Thread {
    public PriorityThread(String name) {
        super(name);
    }

    @Override
    public void run() {
        for (int i = 1; i <= 3; i++) {
            System.out.println(getName() + " running with priority " + getPriority());
        }
    }
}

public class ThreadPriorityDemo {
    public static void main(String[] args) {
        PriorityThread t1 = new PriorityThread("Thread-A");
        PriorityThread t2 = new PriorityThread("Thread-B");
        PriorityThread t3 = new PriorityThread("Thread-C");

        // Setting Priorities
        t1.setPriority(Thread.MIN_PRIORITY);   // 1
        t2.setPriority(Thread.NORM_PRIORITY);  // 5
        t3.setPriority(Thread.MAX_PRIORITY);   // 10

        t1.start();
        t2.start();
        t3.start();
    }
}

## OUTPUT:

Thread-C running with priority 10
Thread-C running with priority 10
Thread-C running with priority 10
Thread-B running with priority 5
Thread-B running with priority 5
Thread-B running with priority 5
Thread-A running with priority 1
Thread-A running with priority 1
Thread-A running with priority 1

## RESULT:
Program executed executed successfully.
