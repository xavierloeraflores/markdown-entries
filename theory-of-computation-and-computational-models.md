---
title: "Theory of Computation & Computational Models"
date: 2023-11-27T19:14:50-08:00
draft: false
tags:
  [
    "Computer Science",
    "Theory of Computation",
    "Automata Theory",
    "Automaton",
    "Computational Models",
    "Finite State Machine",
    "Pushdown Automaton",
    "Linear Bounded Automaton",
    "Turing Machine",
    "Algorithms",
  ]
categories: ["Computer Science"]
---

When solving problems in computer science, it can help to abstract the problem to gain a better understanding of what we can possibly achieve. This can especially be seen when analyzing algorithms since we usually care more about how algorithms would perform on abstract computers (machines) rather than specific hardware.

Computation
: any type of calculation that may include both arithmetical & non-arithmetical steps to provide a solution to a problem.

Computational Models
: abstract models that allow us to reason about what can and can't possibly be computed by a particular device.

---

# 4 Major Models of Automaton

There are many computational models that exists and can all be used for different purposes. There following are 4 major models that are commonly used in order from simplest to most complex:

- Finite State Machine
- Pushdown Automaton
- Linear Bounded Automaton
- Turing Machine

---

## Finite State Machine

Finite State Machines are simple due to the fact that their state is finite, usually in binary which has only two possible states: **0** or **1** and because they have a finite number of possible input sets.

#### Finite State Machine Properties:

- Finite states
- Finite input sets
- Ideal for small amounts of memory
- For analysis of mathematical problems
- For recognizing regular languages
- Handle Type-3 grammars & regular languages

#### Finite State Machine Tuples:

- Q : Finite set of states
- Σ : Set of Input Symbols
- q0 : Initial State
- F : Set of Final States
- σ : Transition Function

---

## Pushdown Automaton

Pushdown Automata can be seen as a Finite State Machine but with an added stack storage. Just like a Finite State Machine, it features the same tuples except with the added initial stack top.

#### Pushdown Automaton Properties:

- Utilizes a stack
- Stack Alphabet
- Initial stack top
- For a collection of elements
- For theories to determine what machines can compute
- Handles Type-2 grammars & context-free languages

#### Pushdown Automaton Tuples:

- Q : Finite set of states
- Σ : Set of Input Symbols
- r : Stack alphabet
- q0 : Initial State
- F : Set of Final States
- σ : Transition Function
- Z : Initial stack top symbol

---

## Linear Bounded Automaton

Linear-bounded automaton consists of two endmarkers with input in between that can be seen as a tape containing data between the endmarkers. A Linear-bounded automaton is a **multi-track non-deterministic Turing machine** with a tape bounded to a finite length.

#### Linear Bounded Automaton Properties:

- Two endmarkers
- Tape alphabet instead of a stack alphabet
- Handles Type-1 grammars & context-sensitive languages

#### Linear Bounded Automaton Tuples:

- Q : Finite set of states
- X : Tape Alphabet
- Σ : Set of Input Symbols
- q0 : Initial State
- F : Set of Final States
- δ : Transition Function
- Ml : Left-end Marker
- Mr: Right-end Marker

---

## Turing Machine

Turing Machines are the most complex family of automaton consisting of finite automaton with infinite storage while having the ability to change symbols on its tape. It is thought to model all computations that can be handled by modern computers.

#### Turing Machine Properties:

- Finite automaton
- Infinite storage
- Changing symbols
- Handles Type-0 grammars & recursively enumerable languages

#### Turing Machine Tuples:

- Q : Finite set of states
- Γ : Tape Alphabet
- Σ : Set of Input Symbols
- q0 : Initial State
- F : Set of Final States
- δ : Transition Function
- H : Halting states |⊆ Q (Subset of Q)
