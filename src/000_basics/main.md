# Understanding the Core C++ Program

The most simple program we can write in C++ is an empty `main` function. This function is also at the core of every C++ program. In this guide, we will look at understanding what the `main` function is and what role it plays in C++ software.

## Contact Information

- Email - CoffeeBeforeArch@gmail.com
- Twitter - @AcceleratorNick

# The Most-Basic C++ Program

Below is the most-basic C++ program - a (mostly) empty `main` function:

```cpp
int main() {
  return 0;
}
```

## What is a function?

Before we can talk about the things that make the `main` function special, we must first understand what a function is.

Put simply, a function is a named routine in our code that we can call on to execute some action (lines of C++). We can further break the function into four parts:

1. A return type
 - The type of value that will be returned to the call-site by the function upon exit
2. A name
 - The name we will use later in the code when we want to execute the function
3. An optional list of parameter types with names
 - Types and names of parameters we want to pass into the function
4. A body
 - The C++ code within the function that will be executed when the function is called

Together, the name and parameter list make up what is known as the function signature. Functions in C++ must be unique in that there may be no two functions with the same function signature.

## What makes the `main` function special

The primary reason the `main` function is special is because it is logically where every C++ program begins. When you execute your program, it starts at `main` (outside of some initialization that occurs before main, but that's a story for another time).

## How many different forms can the `main` function take?

The `main` function can only have one of two function signatures.

The first signature takes 0 parameters:

```cpp
int main() {
  return 0;
}
```

This first form is the one we will typically use in our programs.

The second function signature for `main` takes 2 parameters:

```cpp
int main(int argc, char* argv[]) {
  return 0;
}
```

The form is used when we want to pass in arguments from the command line. `argc` is the integer number of arguments passed from the command line, and `argv` is an array containing those arguments in the form of strings.

## Why does the `main` function typically have `return 0;`?

The return value of the `main` function represents the exit code of the program. A returned value of 0 indicates that a program completed successfully. A non-zero return code is typically used to indicate some kind of error.

From a command line, we can check the value of a return code using `echo $?`:

```txt
cba@cba$ ./main
cba@cba$ echo $?
0
```

If we were to return a different value (e.g., `return 7;`), we would see whatever that number is from when we ran `echo $?`:

```txt
cba@cba$ ./main
cba@cba$ echo $?
7
```

# Compilation and Execution

Before we can execute our program, it must first be transformed from our high-level C++ into an executable (something that can execute on our CPU). This is done with a piece of system software called a compiler.

## What are "compilers"

In reality, the process commonly referred to as compilation is a multi-step process, of which compilation is just one part. In general, there are 4 phases of transforming a piece of C++ into and executable including:

1. Preprocessing
2. Compilation
3. Assembly
4. Linking

Similarly, what we commonly refer to as compilers (e.g., `g++`) are really compiler drivers. There are called compiler drivers because they drive the entire flow of generating things like executables in an automatic way (not just the actual compilation step).

## How can be generate an executable with `g++`?

For our simple program with a (nearly) empty `main` function, we can generate an executable with the following command:

```txt
cba@cba$ g++ main.cpp -o main.out
```

Here, we are feeding our source file to `g++`, and specify the name of our executable using the `-o` flag.

## Executing our program

We can execute our program from the command line by simply running `./main.out` from the command line:

```txt
cba@cba$ ./main.out
```

Unsurprisingly, nothing happens after we press enter! That's because our `main` function only does `return 0;` (returning that the program completed successfully).

# Conclusion

Below are some of the core ideas from this guide:

1. A function is named routine that we can call to execute some set of actions
2. The `main` function is a special kind of function that is where you program begins execution
3. We use compilers to translate our C++ into executables that can execute on our processors

