---
title: "Bubble Sort"
date: 2024-06-01T00:00:00-08:00
draft: false
tags:
  ["Computer Science", ""Algorithms", "Sorting", "Bubble Sort"]
---

## Bubble Sort

Bubble Sort is a simple sorting algorithm which repeatedly compares and swaps adjacent elements in place. By swapping elements into the correct order, larger elements will be bubbled towards the end of the list. Effectively, the algorithm bubbles the current largest element to the end of the list in each phase of the algorithm. Although this algorithm is simple, it is not efficient for larger lists.

## Key Points

<!-- - Time Complexity: O(n^2) -->

Time Complexity: $O({n}^{2})$

<!-- - Space Complexity: O(1) -->

Space Complexity: $O(1)$

<!-- Max Total # of Passes: n-1 -->

Total # of Passes: $n-1$

<!-- Total # of Comparisons: $n*(n-1)/2 -->

Total # of Comparisons: $\frac{n(n-1)}{2}$

Features:

-   Traverses from left to right swapping larger elements to the right
-   Largest element is bubbled to the end of the list in each phase
-   Process is repeated until the list has been sorted

## Pseudocode

```
# Input: An array of integers
# Output: An array of integers sorted in ascending order
# n is the length of the array
BubbleSort(arr):
    for i = 0 to n-1
        for j = 0 to n-i-1
            if arr[j] > arr[j+1]
                swap arr[j] and arr[j+1]
    return arr
```

## Implementation

```typescript
const BubbleSort = (arr: number[]): number[] => {
    for (let i = 0; i < arr.length - 1; i++) {
        for (let j = 0; j < arr.length - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    return arr;
};

const testArr = [5, 3, 8, 4, 2];
console.log(BubbleSort(testArr)); // [2, 3, 4, 5, 8]
```

### Optimized Bubble Sort

```typescript
const OptimizedBubbleSort = (arr: number[]): number[] => {
    for (let i = 0; i < arr.length - 1; i++) {
        let sorted = true; // Flag to check if the array is already sorted
        for (let j = 0; j < arr.length - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                sorted = false; // If a swap is made, the array is not sorted
            }
        }
        if (sorted) return arr; // If the array is already sorted, return it
    }
    return arr;
};

const testArr = [5, 3, 8, 4, 2];
console.log(OptimizedBubbleSort(testArr)); // [2, 3, 4, 5, 8]
```
