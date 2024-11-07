// Members: Aijelle Gumatin, Rhamztyn Manadao, Mekaiah Joyce C. Ulban, Carl Andrei Verches
// This program simulates a vending machine that sells gum, chocolate, popcorn, and juice.

import java.util.Scanner;

public class VendingMachine {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;
        int gumSold = 0;
        int chocolateSold = 0;
        int popcornSold = 0;
        int juiceSold = 0;

        while (true) {
            // Display menu options
            System.out.println("Please select an option:");
            System.out.println("1. Get Gum");
            System.out.println("2. Get Chocolate");
            System.out.println("3. Get Popcorn");
            System.out.println("4. Get Juice");
            System.out.println("5. Display total sold items so far");
            System.out.println("6. Quit");

            // Get user choice
            choice = scanner.nextInt();

            // Process user choice
            switch (choice) {
                case 1:
                    gumSold++;
                    System.out.println("Here is your gum.");
                    break;
                case 2:
                    chocolateSold++;
                    System.out.println("Here is your chocolate.");
                    break;
                case 3:
                    popcornSold++;
                    System.out.println("Here is your popcorn.");
                    break;
                case 4:
                    juiceSold++;
                    System.out.println("Here is your juice.");
                    break;
                case 5:
                    System.out.println(gumSold + " items of gum sold.");
                    System.out.println(chocolateSold + " items of chocolate sold.");
                    System.out.println(popcornSold + " items of popcorn sold.");
                    System.out.println(juiceSold + " items of juice sold.");
                    break;
                case 6:
                    System.out.println("Thank you for using the vending machine. Goodbye!");
                    scanner.close();
                    return; // Exit the program
                default:
                    System.out.println("Error, options 1-6 only!");
                    break;
            }
        }
    }
}
