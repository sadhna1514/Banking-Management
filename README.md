import java.util.*;
class Banking{
	public static void main(String[] args) {
		Scanner ss = new Scanner(System.in);
		System.out.println("Welcome to ATM ");
		System.out.print("Enter PIN : ");
		int pin = ss.nextInt();
		int balance = 10000;
		int deposit = 0;
		int withdrawl =0;
		if(pin == 1234){
			System.out.println("Select any one option ");
			System.out.println("Check Your Balance--> Press 1");
			System.out.println("Deposit money--> Press 2");
			System.out.println("Withdrawl Money-->  Press 3");
			System.out.print("Press Valid option :");
			int opt = ss.nextInt();
			if( opt == 1){
				System.out.print("Balance is :" + balance);
			}
			else if (opt == 2){
				System.out.print(" Enter Amount: ");
				int dep = ss.nextInt();
				balance = balance - dep;
				System.out.println("Remaining Balance is :" + (balance));
			}
			else{
				System.out.System.out.print("Enter Amount : ");
				int with = ss.nextInt();
				if(with<balance){
				    balance = balance - with;
				    System.out.println("Remaining Balance is : " + (balance));
				}
				else{
				    System.out.println("Insufficint Balance");
				}
			}

		}
		else{
			System.out.println("Incorect PIN---");
		}

	}
}
