---
title: "Modular Exponentiation"
date: 2023-11-29T19:26:13-08:00
draft: false
tags: ["Math", "Modular Arithmetic", "Number Theory", "Modulo", "Exponents"]
categories: ["Mathematics"]
---

You can use modular exponentiation to calculate the remainder of a number raised to a power.

The trick to finding large exponentials is to break them down into smaller ones.

### Example:

Given that $M^2 ≡ 51 (mod 59)$, what is $M^{12} (mod 59)$?

```
M^12 = M^(4+8)
M^12 = M^4 * M^8
M^12 = (M^2)^2 * (M^2)^3✅

M^2 ≡ 51 (mod 59)
M^4 ≡ (M^2)^2 ≡ (51)^2 (mod 59)
M^4 ≡ 2601 (mod 59)
M^4 ≡ 5 (mod 59)✅

M^4 ≡ 5 (mod 59)
M^8 ≡ (M^4)^2 ≡ (5)^2 (mod 59)
M^8 ≡ 25 (mod 59)✅

M^12 = M^4 * M^8
M^12 ≡ [(5 mod 59) * (25 mod 59)]
M^12 ≡ 5*25 (mod 59)
M^12 ≡ 125 (mod 59)
M^12 ≡ 7 (mod 59)✅
```
