// Import necessary classes for threading
class RollNumberTable implements Runnable {
    @Override
    public void run() {
        // Array of student roll numbers
        String[] rollNumbers = {
            "2022-SE-001", "2022-SE-002", "2022-SE-003", "2022-SE-004", "2022-SE-031"
        };

        // Print the Roll Number Table header
        System.out.println("Roll Number Table:");
        // Loop through the roll numbers and print each
        for (String rollNumber : rollNumbers) {
            try {
                Thread.sleep(1000); // Simulate some processing delay (1 second)
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
            // Print each roll number with a delay between prints
            System.out.println(rollNumber);
        }
    }
}

class DateOfBirthTable implements Runnable {
    @Override
    public void run() {
        // Array of student dates of birth
        String[] dobList = {
            "27-January", "15-February", "25-March", "05-April", "10-May"
        };

        // Print the Date of Birth Table header
        System.out.println("Date of Birth Table:");
        // Loop through the dates of birth and print each
        for (String dob : dobList) {
            try {
                Thread.sleep(1000); // Simulate some processing delay (1 second)
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
            // Print each date of birth with a delay between prints
            System.out.println(dob);
        }
    }
}

public class ConcurrentTable {
    public static void main(String[] args) {
        // Create two Runnable objects (for roll numbers and dates of birth)
        RollNumberTable rollNumberTable = new RollNumberTable();
        DateOfBirthTable dobTable = new DateOfBirthTable();

        // Create two threads, one for each Runnable
        Thread rollNumberThread = new Thread(rollNumberTable);
        Thread dobThread = new Thread(dobTable);

        // Start both threads
        rollNumberThread.start();
        dobThread.start();

        try {
            // Wait for both threads to finish (i.e., join them with the main thread)
            rollNumberThread.join();
            dobThread.join();
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }

        // Print a final message once both threads have finished
        System.out.println("\nBoth tables printed concurrently.");
    }
}

