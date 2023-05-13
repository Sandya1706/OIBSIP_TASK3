# OIBSIP_TASK3
ATMInterfaceTask3
import java.util.Scanner;
public class atminterfacetask3 {
    public static void main(String args[]) {
        Scanner intake = new Scanner(System.in);
        int balance = 0;
        int withdraw;
        int deposit;
        while (true) {
            System.out.println("Welcome to the ATM");
            System.out.println("choose 1 for checking Bank Balance");
            System.out.println("choose 2 for Deposite");
            System.out.println("choose 3 for Withdraw");
            System.out.println("choose 4 for Quit");
            int choose = intake.nextInt();
            switch (choose) {
                case 1:     //Present Balance
                    System.out.println("The Present Balance is: " + balance);
                    System.out.println("");
                    break;

                case 2:     //Details of deposite
                    System.out.println("Enter the Amount to Deposit: ");
                    deposit = intake.nextInt();
                    balance = balance + deposit;
                    System.out.println("The Present Balance is: " + balance);
                    System.out.println("");
                    break;

                case 3:     //withdraw details
                    System.out.println("Enter the Amount to Withdraw: ");
                    withdraw = intake.nextInt();
                    if (withdraw <= balance) {
                        balance = balance - withdraw;
                        System.out.println("The Present Balance is: " + balance);
                        System.out.println("");
                    } else if (withdraw == balance) {
                        System.out.println("Present balance is ZERO");
                    } else {
                        System.out.println("Check Your Balance");
                    }
                    break;

                default:
                    System.out.println("You Have Entered Wrong Input");
                    break;
            }
        }

    }

}
