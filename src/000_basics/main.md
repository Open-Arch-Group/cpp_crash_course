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


