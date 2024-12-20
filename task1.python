
package alphabetprinter;
import java.util.concurrent.ThreadLocalRandom;
public class AlphabetPrinter {
    public static void main(String[] args) {
        // Thread to print the alphabets
        Thread printThread = new Thread(() -> {
            for (char ch = 'A'; ch <= 'Z'; ch++) {
                try {
                    // Generate a random number between 100 and 1000 milliseconds
                    int sleepTime = ThreadLocalRandom.current().nextInt(100, 1001);
                    
                    // Print the current character
                    System.out.print(ch + " ");
                    
                    // Sleep for a random time to create fluctuation in printing speed
                    Thread.sleep(sleepTime);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });
        
        // Start the thread
        printThread.start();
        
        // Wait for the thread to finish before ending the main program
        try {
            printThread.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}

    
