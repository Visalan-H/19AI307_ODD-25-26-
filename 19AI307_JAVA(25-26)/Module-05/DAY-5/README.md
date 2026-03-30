# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## AIM:
Ensure that multiple threads access shared resources safely without causing inconsistent results.

## ALGORITHM :
1.	Create a shared resource class and mark critical operations as `synchronized`.  
2. Define worker threads that use the shared resource.  
3. Start multiple threads to perform repeated operations on the shared resource.  
4. Use `join()` to ensure the main thread waits for all worker threads to finish.  
5. Display the final result to confirm synchronized access prevented conflicts.

#### Developed By: Visalan H
#### Register Number: 212223240183
## PROGRAM:
#### Program to implement a Synchronization concept using Java
## SOURCE CODE:

class Counter {
    private int count = 0;

    // Synchronized method
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

class WorkerThread extends Thread {
    Counter counter;

    WorkerThread(Counter counter) {
        this.counter = counter;
    }

    @Override
    public void run() {
        for (int i = 0; i < 1000; i++) {
            counter.increment();
        }
    }
}

public class SynchronizationDemo {
    public static void main(String[] args) {
        Counter counter = new Counter();

        WorkerThread t1 = new WorkerThread(counter);
        WorkerThread t2 = new WorkerThread(counter);

        t1.start();
        t2.start();

        try {
            t1.join();
            t2.join();
        } catch (InterruptedException e) {
            System.out.println("Thread interrupted: " + e);
        }

        System.out.println("Final Count: " + counter.getCount());
    }
}






## OUTPUT:
Final Count: 2000


## RESULT:
Program executed executed successfully.
