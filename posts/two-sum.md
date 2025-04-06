---
title: "Two Sum"
date: 2024-06-08T15:16:00-08:00
draft: false
tags:
    [
        "Computer Science",
        "Algorithms",
        "Two Sum",
        "Hash Tables",
        "Arrays",
        "Data Structures",
    ]
categories: ["Computer Science"]
---

## Problem

https://leetcode.com/problems/two-sum/

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`. You may assume that each input would have exactly one solution, and you may not use the same element twice. You can return the answer in any order.

### Examples

Example 1:

```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```

Example 2:

```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

Example 3:

```
Input: nums = [3,3], target = 6
Output: [0,1]
```

## Solutions

The following solutions all exit as soon as a solution is found to optimize it a little further. If no solution is found, the function returns `[-1, -1]` even though the problem states that there is exactly one solution. This is done to highlight a potential edge case where no solution is found in other versions of the problem.

### Solution 1: Brute Force

```typescript
function twoSum(nums: number[], target: number): number[] {
    for (let i = 0; i < nums.length - 1; i++) {
        for (let j = i + 1; j < nums.length; j++) {
            if (nums[i] + nums[j] == target) {
                return [i, j];
            }
        }
    }
    return [-1, -1];
}
```

<!-- Space Complexity: O(1) -->

Space Complexity: $O(1)$

<!-- Time Complexity: O(n^2) -->

Time Complexity: $O(n^2)$

This solutions adds every element in array with every other element in the array until it finds a solution equal to the target. This brute force approach is not time efficient but has a constant space complexity.

### Solution 2: Two-pass Hash Table

```typescript
function twoSum(nums: number[], target: number): number[] {
    const solutions = {};
    for (let i = 0; i < nums.length; i++) {
        let cur = nums[i];
        solutions[cur] = i;
    }
    for (let i = 0; i < nums.length; i++) {
        let cur = nums[i];
        let diff = target - cur;
        if (solutions[diff] !== undefined && solutions[diff] !== i) {
            return [solutions[diff], i];
        }
    }
    return [-1, -1];
}
```

<!-- Space Complexity: O(n) -->

Space Complexity: $O(n)$

<!-- Time Complexity: O(n) -->

Time Complexity: $O(n)$

By implementing a hash table, the time complexity of the problem is greatly reduced down from quadratic to linear time complexity. This comes at the cost of a linear space complexity instant of constant. This solution is commonly known as the "Two Pass Hash Table" since it requires two passes through the array. One pass to create the hash table with indices and the second pass to find the solution.

### Solution 3: One Pass Hash Table

```typescript
function twoSum(nums: number[], target: number): number[] {
    const solutions = {};
    for (let i = 0; i < nums.length; i++) {
        let cur = nums[i];
        let diff = target - cur;
        if (solutions[diff] !== undefined) {
            return [solutions[diff], i];
        } else {
            solutions[cur] = i;
        }
    }
    return [-1, -1];
}
```

<!-- Space Complexity: O(n) -->

Space Complexity: $O(n)$

<!-- Time Complexity: O(n) -->

Time Complexity: $O(n)$

The One Pass Hash Table solution is an optimized version of its Two Pass counterpart. This solution instead only requires one pass through the array and creates the has table as it grows. Although it shares the same space and time complexities, it is more efficient than the Two Pass Hash Table solution through since it implements a pattern where we maintain a hash table of seen elements.
