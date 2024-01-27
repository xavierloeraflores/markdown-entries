---
title: "Big O, Omega, & Theta"
date: 2023-11-17T11:16:51-08:00
draft: false
---

## Big O

Big O is used to to represent the general asymptotic growth of an algorithm. These algorithms are measured as a factor of `O(n)`. When representing a function in Big O, it is common to leave out any constant factors of `n` as well as any other constant atomic operations. A function that runs in `3n^2 + 5` will be represented as `O(n^2)`since we only care about the asymptotic growth of a function.

## Big Ω (Omega)

Big Ω is used to represent the lower bound of a function's asymptotic growth. This means that Big Ω will give use the complexity of a functions best case scenario. Algorithms will be measure as a factor of `Ω(n)` and factor in atomic operations and constant multiples of `n`.

## Big Θ (Theta)

Big Θ represents the average case or random case of a function. It gives us an idea of how an algorithm will perform in any case.

### The relationship between Θ, Ω, O

Given a function `f(n)`, `Ω` represents the lower bound of the function, `O` represents the upper bound, and `Θ` can represent the average case or any case:

$$
Ω(f(n)) ≤ Θ(f(n)) ≤ O(f(n))
$$

$$
Ω(n) <= Θ(n) <= O(n)
$$
