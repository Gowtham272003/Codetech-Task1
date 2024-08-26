import java.util.Scanner;

public class cal {

    public static void main(String[] args) {
        double num1,num2;
        char operator;
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the first number: ");
        num1 = sc.nextDouble();
        System.out.print("Enter the second number: ");
        num2 = sc.nextDouble();
        System.out.print("Choose an operator (+, -, *, /): ");
        operator = sc.next().charAt(0);
        double result;
        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println("The result of addition is: " + result);
                break;
            case '-':
                result = num1 - num2;
                System.out.println("The result of subtraction is: " + result);
                break;
            case '*':
                result = num1 * num2;
                System.out.println("The result of multiplication is: " + result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("The result of division is: " + result);
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                }
                break;
            default:
                System.out.println("Error: Invalid operator.");
                break;
        }
    }
}
