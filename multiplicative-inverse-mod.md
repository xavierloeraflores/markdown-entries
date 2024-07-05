---
title: "Multiplicative Inverse Mod"
date: 2023-11-29T18:45:42-08:00
draft: false
tags: ["Math", "Modular Arithmetic", "Number Theory", Modulo"]
categories: ["Mathematics"]
---

Multiplicative Inverse Modulo
: The multiplicative inverse of $x \mod y$ is a number $n ∈ Z+$ such that $xn\mod y=1$

## Finding the Multiplicative Inverse Modulo:

Given $x$ & $y$, to find the multiplicative inverse, $n$ of $x mod y$ you must find:
$$xn \mod y = 1$$
$$or$$
$$xn ≡ 1 (mod\ y)$$

Substitute values of n to find congruence:

```
x * A1 ≡ B1 !≡ 1 (mod 33)
x * A2 ≡ B2 !≡ 1 (mod 33)
x * A3 ≡ B3 !≡ 1 (mod 33)
x * A4 ≡ B4 ≡ 1 (mod 33) ✅
n = A4 is the multiplicative inverse
```

#### Example:

```
Find the multiplicative inverse of 13 mod 33
From the following set of numbers:
{2, 10, 18, 26, 4, 12, 20, 28}


13 * 2 ≡ 26 !≡ 1 (mod 33)
13 * 10 ≡ 130 !≡ 1 (mod 33)
13 * 28 ≡ 364 ≡ 1 (mod 33) ✅
```
