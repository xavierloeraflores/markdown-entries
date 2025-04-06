---
title: "Exponents Digits"
date: 2023-11-28T19:56:47-08:00
draft: false
tags: ["Math", "Exponents"]
categories: ["Mathematics"]
---

## Finding the ones digit of large exponents

There is a trick to finding the ones place digit of a large exponentiated number. This trick involves finding the values of the small powers to find a pattern. Steps to finding the ones digit:

```
Let A = n^x
Find n^1, n^2, n^3, n^4,...,n^y

Such that the values begin to repeat themselves in a pattern.

Note: The ones digit of n^1 = the ones digit of n^y

Use modulo arithmetic to find the remainder z
z = x%y

Ones digit of n^x = The ones digit n^z
```

#### Example:

```
Find Ones digit of 3^902
x = 902

3^1 = 3 | 3
3^2 = 9 | 9
3^3 = 27 | 7
3^4 = 81 | 1

Ones digit 3^4 = Ones digit 3^1
y = 4

z = 902 % 4 = 2
The ones digit of 3^902 = The ones digit 3^2
Ones digit =  9

```

## Finding the first digits of large exponents

There is a trick to finding the first few digits of a large exponentiated number. This trick does have some degree of error and becomes less accurate the more digits you need. Steps to find the first few digits:

```
Let A = n^x
log10(A) = log10(n^x)
log10(A) = x*log10(n)

# Calculate x * log10(n) as B
log10(A) = B
A = 10^B

# Factor 10^B as two terms of 10^(B-y) & 10^(y)
# Such that B-y ∈ Z & 0<y<1
A = 10^(B-y) * 10^y

#Calculate 10^y as C to form our equation into scientific notation
A = C * 10^(B-y)

First digits of n^x are the digits of C
```

#### Example:

```
Let 𝐴=7^2009
A=7^2009


log10(A)=log10(7^2009)
log10(A)=2009*log10(7)

# Calculate x * log10(n)
log10(A)≈1697.801962
A=10^1697.801962

#Factor 10^B -> 10^(b-y)* 10^y
A=10^1697×10^0.801962
A=6.3381×10^1697

First digits are C= 6.3381

```
