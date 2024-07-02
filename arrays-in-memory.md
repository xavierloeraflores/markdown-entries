---
title: "Arrays in Memory"
date: 2024-07-01T22:19:50-08:00
draft: false
tags:
    [
        "Computer Science",
        "Data Structures",
        "Arrays",
        "RAM",
        "Memory",
        "Lists",
        "Memory",
        "Python",
        "RAM",
    ]
---

Arrays are a data structure used to store a collection of elements of the same type. They are stored in memory continuously. This means that all the elements of the array can be found sequentially in memory.

## Arrays in RAM

Array elements are stored sequentially in memory. The memory address of the first element of the array is used to access the entire array.

The size of the data between each element in the array is determined by the size of the data type of the elements. For example, if the elements are integers, each element will be 4 bytes apart whereas characters will be 1 byte apart.

### Example

Given the following arrays this is how they would be stored in memory:

`arr1 = ['a','b','c']`

| Index:   | 0   | 1   | 3   |
| -------- | --- | --- | --- |
| Value:   | a   | b   | c   |
| Address: | $0  | $1  | $2  |

`arr2 = [4,7,9]`

| Index:   | 0   | 1   | 3   |
| -------- | --- | --- | --- |
| Value:   | 4   | 7   | 9   |
| Address: | $0  | $4  | $8  |

The array `arr1`contains elements of type `char` which are 1 byte each. The memory addresses are of the elements are `$0`, `$1`, and `$2` which are sequentially spaced 1 byte apart. However, since `arr2` contains elements of type `int` which are 4bytes each, the memory addresses are sequentially spaced 4 bytes apart as apposed to array with 1 byte characters.

## Arrays vs Lists

In python, arrays and lists are similar but have some key differences.Arrays will contain elements of the same type while lists can contain elements of different data types. Arrays are more memory efficient and faster than lists because arrays are stored in a continuous block of memory whereas lists are stored in different blocks of memory since they may contain elements of different data types.
