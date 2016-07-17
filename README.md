# JavaSess4Ass2

package Basic;

import java.util.Arrays;
import java.util.Scanner;

public class Sess4Ass2 {
	public static void main(String[] args) {
		int insert;
		// TODO Auto-generated method stub
		System.out.println("Sort of array before insertion");
		int arr[] = { 11, 222, 14, 9, 10 };
		Arrays.sort(arr);
		printArray("Sorted array", arr);

		System.out.println();
		
		Scanner input = new Scanner(System.in);
		System.out.println("Do you want to insert an element ? (Y or N)");
		String yesno = input.next();
		if (yesno.equalsIgnoreCase("Y")) {
			System.out.print("Enter Element to be Insert : ");
			Scanner element = new Scanner(System.in);
			insert = element.nextInt();
			arr[0]=insert;
			System.out.println();
			System.out.println("Sort of array after insertion");
			Arrays.sort(arr);
			printArray("Sorted array", arr);
			

		} else {
			System.out.println("No new element inserted");
			
		}

	}

	private static void printArray(String string, int[] arr) {
		for (int i = 0; i < arr.length; i++) {
			if (i != 0) {
				System.out.print(", ");
			}
			System.out.print(arr[i]);
		}
		System.out.println();
	}
}
