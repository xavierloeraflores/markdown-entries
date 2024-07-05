---
title: "In Place Algorithms"
date: 2024-06-08T12:28:00-08:00
draft: false
tags:
    [
        "Computer Science",
        "Algorithms",
        "In Place",
        "In Place Algorithms",
        "In Place Sorting",
        "Out of Place",
        "Out of Place Algorithms",
        "Out of Place Sorting",
        "Sorting Algorithms",
    ]
categories: ["Computer Science"]
---

## In Place Algorithms

In place algorithms are algorithms that are executed without needing extra memory. They will modify the input data directly and work within the same memory space. In place algorithms can use a amount of extra memory and still be considered in place. As long as the output is stored in the same memory space as the input, the algorithm is considered in place. Algorithms that don't modify the input data directly and require extra memory are considered out of place or not in place.

## Use Case

You would use an in place algorithm when you are working to optimize memory usage. Since in place algorithms do not require extra memory, they are more memory efficient when working with large datasets if memory usage is a concern.

For example, when reversing an array, you can either use a out of place algorithm to return a new reversed array or use an in place algorithm to reverse the input array in the same memory space and return it.

## Out of Place Implementation

```typescript
function reverseArray(arr: number[]): number[] {
    let newArr: number[] = [];

    for (let i = arr.length - 1; i >= 0; i--) {
        newArr.push(arr[i]);
    }

    return newArr;
}

let originalArray = [1, 2, 3, 4, 5];
console.log(originalArray); // [1, 2, 3, 4, 5]
let reversedArray = reverseArray(originalArray);
console.log(reversedArray); // [5, 4, 3, 2, 1]
```

## In Place Implementation

```typescript
function reverseArrayInPlace(arr: number[]): number[] {
    let left = 0;
    let right = arr.length - 1;

    while (left < right) {
        let temp = arr[left]; // Small extra space
        arr[left] = arr[right];
        arr[right] = temp;
        left++;
        right--;
    }
    return arr;
}

let originalArray = [1, 2, 3, 4, 5];
console.log(originalArray); // [1, 2, 3, 4, 5]
let reversedArray = reverseArrayInPlace(originalArray);
console.log(reversedArray); // [5, 4, 3, 2, 1]
```

## Examples

In Place Algorithms:

-   Insertion Sort
-   Bubble Sort
-   Selection Sort
-   Quick Sort
-   Heap Sort

Out of Place Algorithms:

-   Merge Sort
-

## Related Posts

-   [Merge Sort](/notes/posts/merge-sort)
-   [Bubble Sort](/notes/posts/bubble-sort)
