# Simple-Calculator
//A simple calculator which performs basic arithematic operations: Addition, Substraction, Multiplication, Divison.


import java.util.Scanner;

public class SimpleCalculator {

    public static void main(String[] args)        
        Scanner scanner = new Scanner(System.in);

        // Display a menu of operations
        System.out.println("Simple Calculator");
        System.out.println("Select an operation:");
        System.out.println("1. Addition (+)");
        System.out.println("2. Subtraction (-)");
        System.out.println("3. Multiplication (*)");
        System.out.println("4. Division (/)");
        
       
        System.out.print("Enter the operation number (1/2/3/4): ");
        int choice = scanner.nextInt();

        
        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();
        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();

        
        double result = 0;
        switch (choice) {
            case 1: // Addition
                result = num1 + num2;
                System.out.println("Result: " + num1 + " + " + num2 + " = " + result);
                break;
            case 2: // Subtraction
                result = num1 - num2;
                System.out.println("Result: " + num1 + " - " + num2 + " = " + result);
                break;
            case 3: // Multiplication
                result = num1 * num2;
                System.out.println("Result: " + num1 + " * " + num2 + " = " + result);
                break;
            case 4: // Division
                // Check if the second number is not zero to avoid division by zero
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + num1 + " / " + num2 + " = " + result);
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                }
                break;
            default:
                System.out.println("Invalid choice. Please select a valid operation.");
        }

       
    }
}


