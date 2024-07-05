---
title: "Merge Sort"
date: 2024-06-02T00:00:00-08:00
draft: false
tags:
    [
        "Computer Science",
        "Algorithms",
        "Sorting",
        "Merge Sort",
        "Stable Sorting Algorithms",
        "Sorting Algorithms",
    ]
categories: ["Computer Science"]
---

## Merge Sort

Merge Sort is a divide-and-conquer algorithm that divides the input list into two halves, recursively sorts the halves, and then merges the sorted halves. This algorithm is efficient for larger lists and is a stable sorting algorithm that guarantees $O(n \log n)$ time complexity.

## Key Points

<!-- - Time Complexity: O(n log n) -->

Time Complexity: $O(n \log n)$

<!-- - Space Complexity: O(n)  -->

Space Complexity: $O(n)$

Process:

-   Divide: The input list is divided into two halves
-   Conquer: The two halves are recursively sorted
-   Merge: The sorted halves are merged back together in sorted order

Features:

-   Best, Worst, and Average Case Time Complexity: $O(n \log n)$
-   Stable Sorting Algorithm: Maintains the relative order of equal elements
-   Not In-Place: Requires additional space for merging

## Pseudocode

```
# Input: An array of integers
# Output: An array of integers sorted in ascending order
# n is the length of the array
Merge(arrLeft, arrRight):
    sortedArray = []
    while arrLeft.length > 0 or arrRight.length > 0
        if arrLeft.length == 0
            num = arrRight.shift()
            sortedArray.push(num)
        else if arrRight.length == 0
            num = arrLeft.shift()
            sortedArray.push(num)
        else
            if arrLeft[0] < arrRight[0]
                num = arrLeft.shift()
                sortedArray.push(num)
            else
                num = arrRight.shift()
                sortedArray.push(num)
    return sortedArray

MergeSort(arr):
    if n <= 1
        return arr
    mid = n / 2
    left = MergeSort(arr[0:mid])
    right = MergeSort(arr[mid:n])
    return Merge(left, right)
```

## Implementation

Merge()

```typescript
function Merge(arrLeft: number[], arrRight: number[]): number[] {
    const sortedArray: number[] = [];
    while (arrLeft.length > 0 || arrRight.length > 0) {
        if (arrLeft.length == 0) {
            const num = arrRight.shift() || 0;
            sortedArray.push(num);
        } else if (arrRight.length == 0) {
            const num = arrLeft.shift() || 0;
            sortedArray.push(num);
        } else {
            if (arrLeft[0] < arrRight[0]) {
                const num = arrLeft.shift() || 0;
                sortedArray.push(num);
            } else {
                const num = arrRight.shift() || 0;
                sortedArray.push(num);
            }
        }
    }
    return sortedArray;
}

const arr1 = [1, 3, 5];
const arr2 = [2, 4, 6];
console.log(Merge(arr1, arr2)); // [1, 2, 3, 4, 5, 6]
```

MergeSort()

```typescript
function MergeSort(arr: number[]): number[] {
    if (arr.length <= 1) return arr;

    const mid = Math.floor(arr.length / 2);
    const left = MergeSort(arr.slice(0, mid));
    const right = MergeSort(arr.slice(mid));

    return Merge(left, right);
}

const testArr = [5, 3, 8, 4, 2, 7, 1, 6];
console.log(MergeSort(testArr)); // [1, 2, 3, 4, 5, 6, 7, 8]
```

### Optimized Merge Sort

Merge()

```typescript
function Merge(arrLeft: number[], arrRight: number[]): number[] {
    const sortedArray: number[] = [];
    // Initialize indices for left and right arrays
    let leftIndex = 0;
    let rightIndex = 0;

    while (leftIndex < arrLeft.length && rightIndex < arrRight.length) {
        if (arrLeft[leftIndex] < arrRight[rightIndex]) {
            sortedArray.push(arrLeft[leftIndex]);
            leftIndex++;
        } else {
            sortedArray.push(arrRight[rightIndex]);
            rightIndex++;
        }
    }
    // Concatenate the remaining elements from the left and right arrays
    return sortedArray
        .concat(arrLeft.slice(leftIndex))
        .concat(arrRight.slice(rightIndex));
}
```

MergeSort()

```typescript
function MergeSort(arr: number[]): number[] {
    if (arr.length <= 1) return arr;

    const mid = Math.floor(arr.length / 2);
    const left = MergeSort(arr.slice(0, mid));
    const right = MergeSort(arr.slice(mid));

    return Merge(left, right);
}

function Merge(arrLeft: number[], arrRight: number[]): number[] {
    const sortedArray: number[] = [];
    // Initialize indices for left and right arrays
    let leftIndex = 0;
    let rightIndex = 0;

    while (leftIndex < arrLeft.length && rightIndex < arrRight.length) {
        if (arrLeft[leftIndex] < arrRight[rightIndex]) {
            sortedArray.push(arrLeft[leftIndex]);
            leftIndex++;
        } else {
            sortedArray.push(arrRight[rightIndex]);
            rightIndex++;
        }
    }
    // Concatenate the remaining elements from the left and right arrays
    return sortedArray
        .concat(arrLeft.slice(leftIndex))
        .concat(arrRight.slice(rightIndex));
}
```

## Related Posts

-   [Stable Sorting Algorithms](/notes/posts/stable-sorting-algorithms)
