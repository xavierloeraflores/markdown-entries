---
title: "Greatest Common Divisor & Least Common Multiple"
date: 2023-11-24T19:51:39-08:00
draft: false
tags: ["Math", "Number Theory", "GCD", "LCM", "Prime Numbers"]
---

## Greatest Common Divisor

GCD
: The largest number $n ∈ Z+$ that is a factor of both nonzero $x$ & $y$ such that both $n | x$ & $n | y$ are true.

Relatively Prime
: Two numbers $x$ and $y$ are said to be **relatively prime** if and only if their GCD is 1. In other terms:
$$∄ n ∈ Z+ > 1$$
where both $n | x$ and $n | y$ are true.

## Least Common Multiple

LCM
: The smallest number $n ∈ Z+$ that is a multiple of both nonzero $x$ & $y$ such that both $x | n$ & $y | n$ are true.

## GCD & LCM Prime Factorizations

Let $x,y ∈ Z+$ with prime factorizations that can be expressed using a common set of primes:

<!-- x = P1^α1 * P2^α2 * P3^α3...+ Pr^αr -->

$$ x = P*{1}^{α1} \* P*{2}^{α2} \* P*{3}^{α3}...+ P*{r}^{αr} $$

<!-- y = P1^β1 + P2^β2 + P3^β3...+ Pr^βr -->

$$ y = P*{1}^{β1} + P*{2}^{β2} + P*{3}^{β3}...+ P*{r}^{βr} $$

Then $x$ divides $y$ if and only if $αi≤βi$ for all $1<=i<=r$

<!-- GCD = P1^min(α1,β1) * P2^min(α2,β2) * P3^min(α3,β3)...+ Pr^min(αr,βr) -->

$$ GCD = P*{1}^{min(α1,β1)} \* P*{2}^{min(α2,β2)} \* P*{3}^{min(α3,β3)}...+ P*{r}^{min(αr,βr)}$$

<!-- LCM = P1^max(α1,β1) * P2^max(α2,β2) * P3^max(α3,β3)...+ Pr^max(αr,βr) -->

$$ LCM = P*{1}^{max(α1,β1)} \* P*{2}^{max(α2,β2)} \* P*{3}^{max(α3,β3)}...+ P*{r}^{max(αr,βr)}$$

---

#### Example:

$8 = 2^3 * 3^0$

$6 = 2^1 * 3^1$

<!--  GCD(8,6) = 2^min(3,1) * 3^min(0,1) = 2^1 * 3^0 = 2 -->

$ GCD(8,6) = 2^{min(3,1)} _ 3^{min(0,1)} = 2^1 _ 3^0 = 2$

<!--  LCM(8,6) = 2^max(3,1) * 3^max(0,1) = 2^3 * 3^1 = 24 -->

$ LCM(8,6) = 2^{max(3,1)} _ 3^{max(0,1)} = 2^3 _ 3^1 = 24 $
