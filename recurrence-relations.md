---
title: "Recurrence Relations"
date: 2023-11-20T11:09:14-08:00
draft: false
---


## Recurrence Relations Definition
Recurrence Relation Rule 1
: An equation that expresses the value of `An` in terms of at least one previous term in a sequence.

Recurrence Relation Rule 2
: Initial conditions must be specified to determine the value of the first term in the sequence. 

#### Example:
`An = A(n-1)+ 2* A(n-2)` for `n>= 2` where `A0=2, A1=5`

## Arithmetic Sequences
Given a sequence `A0, A1, A2, A3, ...`, there may be an arithmetic sequence `An` that satisfies the recurrence relation.

#### Example:
`An = A(n-1) + 6` for `n>= 1` where `A0=3`
> - `A1 = A0 + 6 = 3 + 6 = 9 `
> - `A2 = A1 + 6 = 9 + 6 = 15 `
> - `A3 = A2 + 6 = 15 + 6 = 21 `

Notice how each sum is 6 more than the previous sum. We can create an arithmetic sequence from this recurrence relation.

`An = 6n + 3` satisfies the recurrence relation for all values `n>= 0` assuming `A0=3`.


### Fibonacci Sequence
The Fibonacci sequence is a sequence of numbers where each number is the sum of the previous two numbers. The first two numbers in the sequence are `0` and `1`.

Fibonacci Sequence
: `An=A(n-1)+A(n-2)` for `n>=2` where `A0=0` &`A1=1`

## Solving Recurrence Relations
The best way to solve recurrence relations is to find a non-recursive formula for the sequence. Use this closed formula to calculate any value of `An` in the sequence.

Close Formula
: A non-recursive formula to calculate `An` for a sequence.

### Iteration Involving Substitution Method
> - `An = A(n-1) + 3` for `n>= 1` where `A0=2`
> - `A0 = 2`
> - `A1 = A0 + 3 = 2 + 3 =  2+3`
> - `A2 = A1 + 3 = (2+3) + 3 = 2 + 2(3)`
> - `A3 = A2 + 3 = (2+3+3) + 3 = 2 + 3(3)`
> - `A4 = A3 + 3 = (2+3+3+3)+3 = 2+ 4(3)`

For `An`, the sum is `2 + n(3)` where `n>=0`
Solution: `An = 2+3n`

### Iteration Without Substitution Method
> - `An = A(n-1) + 3` for `n>= 1` where `A0=2`
> - `A0 = 2`
> - `A1 = A(n-1) + 3 = A(n-1) + 3`
> - `A2 = (A(n-2) + 3)+3 = A(n-2) + 2(3)`
> - `A3 = (A(n-3) + 2(3))+3 = A(n-3) + 3(3)`
> - `A3 = (A(n-4) + 3(3))+3 = A(n-4) + 4(3)`

For `An`, the sum is `A(n-n) + n(3)` where `n>=0`, meaning that `An = A0 + n(3)`
Solution: `An = 2+3n`