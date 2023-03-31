---
layout: post
title: Two Pointer Template - Data Structures and Algorithms 
description: A core template to memorise for solving two pointer problems in Java
---

Here's a Java template for solving two-pointer problems. The template demonstrates a general approach to solving such problems and can be adapted to fit specific problem requirements.

```
public class TwoPointerProblem {

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5, 6, 7, 8, 9};
        int target = 10;

        twoPointerSolution(arr, target);
    }

    public static void twoPointerSolution(int[] arr, int target) {
        int leftPointer = 0;
        int rightPointer = arr.length - 1;

        while (leftPointer < rightPointer) {
            int currentSum = arr[leftPointer] + arr[rightPointer];

            if (currentSum == target) {
                System.out.println("Found a solution: " + arr[leftPointer] + " + " + arr[rightPointer] + " = " + target);
                leftPointer++;
                rightPointer--;
            } else if (currentSum < target) {
                leftPointer++;
            } else {
                rightPointer--;
            }
        }
    }
}
```

This template can be modified based on the specific problem requirements, such as finding a pair with a given product, finding a subarray with a given sum, or any other problem that requires the two-pointer technique.

Remember that this template assumes the input array is sorted. If the input array is not sorted, you might need to sort it first using Arrays.sort(arr) before applying the two-pointer technique.