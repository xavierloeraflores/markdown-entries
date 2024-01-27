---
title: "Prime & Composite Numbers"
date: 2023-11-20T08:54:34-08:00
draft: false
---

#### Prime & Composite Relationship:
If $p ∈ Z+$ and $p > 1$, then $p$ is either **prime** or **composite**. 

#### Prime Numbers:
If $p ∈ Z+$ and $p > 1$, then $p$ is **prime** if the the only factors of p are $1$ & $p$.

#### Composite Numbers:
If $p ∈ Z+$ and $p > 1$, then $p$ is **composite** if $p$ if $∃ a ∈ Z+$ such that $a | p$ & $1 < a < p$. 


## Fundamental Theorem of Arithmetic
Every integer $a ∈ Z+$ and $a > 1$ is either prime or can be expressed as a unique product of 2 or more primes (*composite*), where the primes are written in non-decreasing order. 
Examples: 
- $12 = 2 * 2 * 3 = 2^2 * 3$
- $200 = 2 * 2 * 2 * 5 * 5 = 2^3 * 5^2$

## Trial Division Theorem
If $n ∈ Z+$ and $n > 1$, then $n$ is prime if and only if $n$ is not divisible by any prime $p$ such that $p ≤ √n$.

If $n ∈ Z+$, $n > 1$ and $n$ is composite, the $n$ has a prime divisor $p$ such that $p ≤ √n$.

If then $n = ab$, where $a ∈ Z+$ such that $1<a<n$ and where $b ∈ Z+$ such that $1<b$. Then $a$ and $b$ are factors of $n$ and $a ≤ √n$ and $b ≤ √n$ because if both $a$ or $b$ are larger than $√n$, then $ab > √n * √n = n$ which is a contradiction.

For any positive composite integer $n$, one of the factors has to be less than or equal to $√n$ because if two factors are greater than $√n$, then the product would be greater than $n$. 
## Other Prime Number Properties
#### Euclid's Theorem
There are infinitely many prime numbers.

Assuming we have the complete set of all primes:
$P1,P2,P3,...,Pn$. We create a composite number that is the product of all the primes in the set:

$Q = P1 * P2 * P3 * .... * Pn$. 
If we add $1$ to the composite number:
$Q + 1= P1 * P2 * P3 * .... * Pn + 1$, then $Q+1$ is either composite or prime. 

Assuming this new number is not prime, then the number is composite meaning it should be divisible by some prime $P < Q+1$. Since it can't be divided by our presumed completed list of primes, then it must be prime which means there must be a prime that is not in the list. 

Therefore, there are infinitely many primes.

[Infinite Primes - Numberphile](https://www.youtube.com/watch?v=ctC33JAV4FI)



#### Prime Number Total Approximation:
The number of primes less than or equal to $x$ is approximately $x/ln(x)$.

![Prime Numbers](/notes/images/prime-numbers.png)
