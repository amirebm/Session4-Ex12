// برنامه ایی بنویسید که آرایه ایی از ورودی خوانده و آن را برعکس نمایش دهد

# Session4-Ex12
package com.personal.Ex12;

import java.util.Scanner;

public class Ex12 {

	public static void main(String[] args) {

		int arrayLength;
		Scanner sc= new Scanner(System.in);
		System.out.println("Enter a the size of array");
		arrayLength=sc.nextInt();
		int[] ar= new int[arrayLength];
		
		System.out.println("Please enter "+ arrayLength+ " numbers for array:");
		
		for (int i = 0; i < ar.length; i++) 
		ar[i]=sc.nextInt();	
		
		System.out.println("The array with Original form");
        printArray(ar);
		System.out.println("The array with Changed form");
        ReverseArray(ar);
        printArray(ar);

	}
	static void  ReverseArray(int[] ar) {

		int temp;
	for (int i = 0; i < (ar.length/2); i++) {
		
		temp=ar[(ar.length-i)-1];
		ar[(ar.length-i)-1]=ar[i];
		ar[i]=temp;
        printArray(ar);

		
	}
	
	}

	static void printArray(int arr[])
    {
        int n = arr.length;
        for (int i=0; i<n; ++i)
            System.out.print(arr[i] + " ");
        System.out.println();
    }

}
