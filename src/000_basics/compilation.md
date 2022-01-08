# Compilation Basics

Before any of our C++ can be executed, it must first be translated into a representation that our processor can understand (an executable). This is done with a piece of system software called the compiler.

In reality, the "compiler" is a collection of tools, and just one step in the process of making an executable is compilation. In this guide, we'll look at the major steps in generating an executable, and understand how they work together.

## Contact Information

- Email - CoffeeBeforeArch@gmail.com
- Twitter - @AcceleratorNick

# The Steps of Generating an Executable

In general, the steps of compilation are:

1. Preprocessing
2. Compilation
3. Assembly
4. Linking

A compiler-driver like `g++` will abstract these steps away from us. However, we can save the intermediate results from each of these steps using the `--save-temps` option:

```txt
cba@cba$ g++ iostream.cpp -o iostream --save-temps
cba@cba$ ls
iostream  iostream.cpp  iostream.ii  iostream.o  iostream.s
```

In addition, we can stop the compiler after each intermediate step using the `-E`, `-S`, and `-c` commands. We'll look at each of these in the following sections

# Step 1: The Preprocessor

# Step 2: The Compiler

# Step 3: The Assembler

# Step 4: The Linker

