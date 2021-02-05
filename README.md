# NetPay
import java.util.Scanner;

public class NetPay {

	public static void main(String[] args) {
			double hoursWorked;
			double grossPay;
			double netPay;
			double Deductions;
			double FEDERAL_TAX_PERCENT = 10.00;
			double STATE_TAX_PERCENT = 4.5;
			double SS_PERCENT = 6.2;
			double MEDICARE_PERCENT = 1.45;
			double PAY_PER_HOUR = 7.25;
			double Federal;
			double State;
			double SocialSecurity;
			double Medicare;
			
			Scanner keyboard= new Scanner(System.in);
			System.out.println("Input number of hours worked");
			
			hoursWorked = keyboard.nextDouble();
			
			grossPay = PAY_PER_HOUR * hoursWorked;
			
			Federal = grossPay / FEDERAL_TAX_PERCENT;
			State = grossPay * STATE_TAX_PERCENT / 100;
			SocialSecurity = grossPay * SS_PERCENT / 100;
			Medicare = grossPay * MEDICARE_PERCENT / 100;
			Deductions = Federal + State + SocialSecurity + Medicare;
			
			netPay = grossPay-Deductions;
			
			System.out.println("Hours per week: \t" + hoursWorked);
			System.out.println("Gross Pay:      \t" + grossPay);
			System.out.println("Net pay:        \t" + netPay);
			System.out.println();
			System.out.println("Deductions");
			System.out.println("Federal:        \t" + Federal);
			System.out.println("State:          \t" + State);
			System.out.println("SocialSecurtiy: \t" + SocialSecurity);
			System.out.println("Medicare:       \t" + Medicare);
			
			
			
			keyboard.close();
	}

}
