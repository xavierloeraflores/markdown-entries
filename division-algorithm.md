---
title: "Division Algorithm"
date: 2023-11-17T13:41:31-08:00
draft: false
---

## Integer Division

Integer division is a division operation that falls under **number theory**, a branch of math that is concerned with studying the properties of integers. In integer division, both the inputs and the output are integers resulting in being able to find an integer quotient and an integer remainder given two other integers.

### Divides

For 2 integers $x$ and $y$, if there is an integer $k$ such that $y=kx$, then $x$ divides, $y$ is a multiple of $x$, $x$ is a factor/divisor of $y$.

This is denoted by the following notation:
$$x | y$$

#### Dividing Linear Combinations

For x, y, & z being integers: If $x | y$ & $x | z$, then $x | (sy + tz)$ for any integers $s$ & $t$.

### Integer Division Definitions

To find the quotient of two integers, $n$ & $d$ use the following formula: `q = n div d`
$$q = n / d$$

To find the remainder of two integers, $n$ & $d$ use the following formula:`r = n mod d`
$$r = n \text{\%} d$$

<!-- r = n % d -->

## The Division Algorithm

For any two given two integers, there is a unique integer quotient and integer remainder that satisfies the following definition:

> Let $n$ be an integer and let $d$ be a positive integer. Then, there are unique integers $q$ and $r$, with $0 ≤ r ≤ d - 1$, such that $n = qd + r$.

### Procedural Version of the Division Algorithm

The following is psuedocode for the division algorithm for an integer $n$ that is positive.

```
# Input: Integers n and d > 0.
# Output: q = n div d, and r = n mod d.
q := 0
r := n
while ( r ≥ d )
      q := q + 1
      r := r - d
end-while
```

### The Division Algorithm with Negative Numbers

When trying to find the quotient and remainder of a negative number, the quotient and remainder will result in different constant values than if the number was positive.

#### Example:

```
44 / 5 = 8
44 % 5 = 4

44 = 8 * 5 + 4
--------------
-44 / 5 = -9
-44 % 5 = 1

-44 = -9 * 5 + 1

```
