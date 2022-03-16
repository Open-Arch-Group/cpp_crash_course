# Getting Started

Before we get started writing C++ code, there are a few background pieces of information that we need to learn ahead of time. In this guide, we'll try and (simply) answer the question "what is C++", and what some of the core elements are.

## What is C++?

Simply put, C++ is a compiled language that is statically typed. The two core parts of that sentence are "compiled" and "statically typed".

### What is a compiled language?

A compiled language is one that requires an extra piece of software (a compiler) to translate your code into a lower-level language before it can execute. We use compilers to translate our high-level C++ into something our underlying CPU can understand (x86 assembly, ARM assembly, etc.).

### What is a statically-typed language?

In a C++, we assign types to variables. These types determine things like how a variable can be used and how much space it take up (in memory).

In a statically-typed language, the types of all variables must be know at compile-time. This means that the user has declared the types for all variables in the program, or in the case of automatic type deduction, the compiler is able to determine the appropriate type for itself.

