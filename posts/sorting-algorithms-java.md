---
title : "Sorting algorithms implementation using Java"
created : "2020-11-28T11:03:00+05:30"
updated : "2020-11-28T11:03:00+05:30"
categories : ["software-engineering"]
tags : ["github"]
summary : "Sorting algorithms implementation using Java"
---

## [Quick Sort](https://www.geeksforgeeks.org/quick-sort/)

```java
public class QuickSort {

	public static void main(String[] args) {
		int[] arr = new int[] { 4, 1, 4, 6, 21, 3, 7, 2, 5, 67, 52, 3, 23, 6, 2, 2 };
		quickSort(arr, 0, arr.length - 1);
		for (int num : arr) {
			System.out.print(num + " ");
		}
	}

	private static void quickSort(int[] arr, int low, int high) {
		if (high <= low) {
			return;
		}
		int pivotIndex = getPivotIndex(arr, low, high);

		quickSort(arr, low, pivotIndex - 1);
		quickSort(arr, pivotIndex + 1, high);
	}

	private static int getPivotIndex(int[] arr, int low, int high) {
		if (low >= high) {
			return low;
		}
		int pivot = arr[low];
		int i = low + 1;
		int j = high;
		while (i < j && i > 0 && j > 0 && i < arr.length && j < arr.length) {
			while (pivot >= arr[i] && i < j) {
				i++;
			}
			while (pivot < arr[j] && i <= j) {
				j--;
			}
			if (i < j) {
				swap(arr, i, j);
			}
		}
		swap(arr, j, low);
		return j;
	}

	private static void swap(int[] arr, int i, int j) {
		int temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}

}
```

## [Selection Sort](https://www.geeksforgeeks.org/selection-sort/)

```java
public class SelectionSort {

	public static void main(String[] args) {
		int[] arr = new int[] { 4, 1, 4, 6, 21, 3, 7, 2, 5, 67, 52, 3, 23, 6, 2, 2 };
		sort(arr);
		print(arr);
	}

	private static void print(int[] arr) {
		for (int num : arr) {
			System.out.print(num + " ");
		}
	}

	private static void sort(int[] arr) {
		for (int i = 0; i < arr.length - 1; i++) {
			int minIndex = findMinimumNumberIndex(arr, i + 1);
			swap(arr, i, minIndex);
		}
	}

	private static void swap(int[] arr, int i, int j) {
		if (i == j) {
			return;
		}
		int temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}

	private static int findMinimumNumberIndex(int[] arr, int startIndex) {
		int minNumber = arr[startIndex];
		int minIndex = startIndex;
		for (int i = startIndex + 1; i < arr.length; i++) {
			if (minNumber > arr[i]) {
				minNumber = arr[i];
				minIndex = i;
			}
		}
		return minIndex;
	}

}
```

```
