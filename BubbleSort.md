#冒泡排序#
###原理：每次循环左右相邻的两个元素进行比较，如果比较的两个数中右边的那个数比左边的小则交换这两个数的位置，依此类推，
最后最右边那个数是排列中的最大数，总共循环比较个数-1次，第二趟比较比较个数-2次

###冒泡排序总的平均时间复杂度为：O(n2) ###


package algorithm;

import java.util.Arrays;

public class Bubble {
	public static void main(String[] args) {
		int[] arr = {45,2,65,32,15,48,52,5};
		System.out.println("排序前的排序:"+Arrays.toString(arr));
		arr = fun(arr);
		System.out.println("排序后的排序:"+Arrays.toString(arr));
	}

	private static  int[] fun(int[] arr) {
		for (int i = 1; i < arr.length; i++) {
			for (int j = 0; j < arr.length-i; j++) {
				if (arr[j+1]<arr[j]) {
					int temp = 0;
					temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp;
				}
			}
		}
		return arr;
	}
}