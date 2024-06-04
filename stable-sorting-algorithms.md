---
title: "Stable Sorting Algorithms"
date: 2024-06-04T00:00:00-08:00
draft: false
tags:
    [
        "Computer Science",
        "Algorithms",
        "Sorting",
        "Stable Sorting Algorithms",
        "Stable Sorting",
        "Sorting Algorithms",
        "Merge Sort",
        "Bubble Sort",
        "Insertion Sort",
        "Count Sort",
        "Tim Sort",
        "Quick Sort",
        "Selection Sort",
        "Heap Sort",
    ]
---

## Stable Sorting Algorithms

Stable sorting algorithms are algorithms that maintain the relative order of equally valued elements in its sorted output. This means that if two elements are equal in value, the element that appears first in the original list will appear first in the sorted list.

## Use Case

One use case when sorting a list of objects by multiple keys. If the list is sorted by one key and then sorted by another key, the relative order of the first key will be maintained in the second sort.

Example: you want to maintain the previously alphabetically sorted list of names when sorting by age.

## Examples

Stable Sorting Algorithms:

-   Merge Sort
-   Bubble Sort
-   Insertion Sort
-   Count Sort
-   Tim Sort

Unstable Sorting Algorithms:

-   Quick Sort
-   Selection Sort
-   Heap Sort

> 🗒️ **Note:** There exists implementations of these algorithms such as Quick Sort that may fall into the other category but typically most implementations of these listed algorithms fall under the categories listed above.

### Convert Unstable to Stable

It is possible to convert an unstable sorting algorithms into a stable sorting algorithm by modifying the algorithms to factor in the original order and position of elements. One example of this is to alter the comparison algorithm to keep the original order of elements via a secondary comparison of the original index of the elements.

## Related Posts

-   [Merge Sort](/notes/posts/merge-sort)
-   [Bubble Sort](/notes/posts/bubble-sort)
