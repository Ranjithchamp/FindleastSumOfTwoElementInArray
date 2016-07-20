# FindleastSumOfTwoElementInArray
package guvi;

import java.util.Scanner;

public class FindClosetNumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner qq = new Scanner(System.in);
		System.out.println("enter size of array");
		int nn = qq.nextInt();
		int count[] = new int[nn];
		System.out.println("enter array element");
		for (int i = 0; i < nn; i++) {
			count[i] = qq.nextInt();
		}
		int sum;
		int g = 0, n = 0, h = 0;
		for (int i = 0; i < nn; i++) {
			for (int j = i + 1; j < nn; j++) {
				sum = 0;
				sum = count[i] + count[j];
				if (sum < 0) {
					sum = sum * -1;
				}
				if (i == 0 && j == 1) {
					n = sum;
					g = i;
					h = j;
					break;
				}
				if (sum < n) {
					n = sum;
					g = i;
					h = j;
					break;
				}
			}
		}
		System.out.println("The two elements are " + count[g] + " and "
				+ count[h]);

	}
}
