---
title: "Modulo N Congruence & Arithmetic"
date: 2023-11-24T07:40:29-08:00
draft: false
tags: ["Modulo", "Congruence", "Arithmetic", "Math", "Number Theory"]
---

## Congruence Modulo n

Congruence Modulo N
Let $n ∈ Z+ > 1$. Let $(x, y) ∈ Z$. Then **x is congruent to y modulo n** if $x \text{\%} n = y \text{\%} n$. This congruence is denoted as:
$$x≡y(mod n)$$

#### Example:

```
x mod n = y mod n
x = 20, y = 10, n = 5
20 % 5 = 10 % 5
0 = 0
20 ≡ 10(mod 5)
```

Alternate Congruence Characterization
: Let $n ∈ Z > 1$. Let $(x,y) ∈ Z$.
$x≡y(mod n)$
if and only if $n |(x-y)$

#### Example:

```
n | (x-y)
x = 20, y = 10, n = 5
5 | (20-10)
5 | 10 ✅
20 ≡ 10(mod 5)
```

## Modulo n Arithmetic

### Modulo Arithmetic: Exponential Numbers

Since a number that is raised to any positive integer power is simply a multiple of itself. There is no need to to find the solve the fully exponent number when solving for the modulo of that exponent number.

Exponential Modulo Arithmetic
: $x^y \text{\%} n = (x \text{\%} n)^y \text{\%} n$

<!-- x^y % n = (x % n)^y % n -->

When applied in the the world of computer science, we are able to avoid errors caused by overflows when dealing with numbers raised to large powers. The number `13^170 mod 18` would surely result to a large number that would be inefficient to compute if we computed `13^170` before then taking the `mod 18` of that result. We can instead repeated apply `mod 18` to a product 170 times to keep the working set of integer values low.

```
#Partial Results
p:= 13
For i:=1 to 170
    p:=(13*p) mod 18
End - for

Return p
```

### Modular Arithmetic Operations

Let $n ∈ Z > 1$. Let $(x, y) ∈ Z$, then:

<!-- [x%n + y%n]%n = [x+y]%n -->
$$[x\text{\%}n + y\text{\%}n]\text{\%}n = [x+y]\text{\%}n$$
<!-- [x%n * y%n]%n = [x*y]%n -->
$$[x\text{\%}n * y\text{\%}n]\text{\%}n = [x*y]\text{\%}n$$

#### Example:

```
(651^123 + 17) mod 10
(651^123 + 17)  % 10
((651%10)^123 + 17%10)
((1)^123 + 7)
(1+7) = 8
(651^123 + 17)  % 10 = 8
```
