import java.util.Scanner;


public class DavisStore_Hw {

	public static void main(String[] args) {

		Scanner sc = new Scanner(System.in);

		System.out.print("What do you sell? ");
		String item = sc.nextLine();

		System.out.print("How much do " + item + " cost? $ ");
		double cost = sc.nextDouble();

		System.out.print("How many days do you want to play? ");
		int num = sc.nextInt();

		for (int i = 0; i < num; i++)
		{
		int rands = (int) (Math.random() * 25 -1);
		System.out.println("\n\nToday you sold " + (rands) + " " + item );
		System.out.print("You made $" + (cost * rands));

		int davisrands = (int) (Math.random() * 9 -3);
		int daviscostrands = (int) (Math.random() * 3);
		double davisprice = (cost -= daviscostrands);
		System.out.print("\nYour Main Empire is Dictator Davis' Super Awesome Store");

		if((davisprice) < 0)
		{
			davisprice = 0;
		}
		if(davisrands < 0)
		{
			davisrands = 0;
		}
		
		
		System.out.print("\nToday they sold " + (rands + davisrands) + " " + item + " and made $" + (davisprice * davisrands));

		if((cost * rands) > (davisprice * davisrands))
		{
			System.out.println("\nCongrats! You beat the Dictator today ;)");
		}
		if((cost * rands) < (davisprice * davisrands))
		{
			System.out.println("\nBetter luck next time loser :( ");
		}
		if((cost * rands) == (davisprice * davisrands))
		{
			System.out.println("\nYou guys made the same amount of money :|");
		}


	}

}
	}
	
