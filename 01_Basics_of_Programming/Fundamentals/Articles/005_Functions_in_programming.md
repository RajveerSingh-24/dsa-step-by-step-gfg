# Functions in Programming (Java)

## What is a Function?
A **function** is a reusable block of code that performs a specific task. Functions help make programs organized, reduce code repetition, and improve readability.

In Java, functions are called **methods**. They are defined inside a class and are executed when they are called.

## Syntax

```java
returnType functionName(parameters) {
    // code to execute
    return value;
}
```
## Example: Function in Java

```java
public class Main {

    // Function to add two numbers
    static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int result = add(5, 3);

        System.out.println("Sum: " + result);
    }
}
```
## Output
```
5
```

---
# Types of Functions
## Based on Origin:
- Built-in functions: These predefined functions provided by programming languages or libraries to perform common tasks such as mathematical calculations, input/output, or string operations.
- User-defined: These functions are functions written by programmers to perform specific tasks required in a program.

## Based on Data Flow
- No Arguments, No Return Value
- Arguments, No Return Value
- No Arguments, With Return Value
- Arguments, With Return Value

---
# Advantages of Functions
- Code reusability
- Better program structure
- Easier debugging
- Reduces code duplication
- Improves readability

---
# Key Points
- Functions in Java are called methods.
- A function can take inputs using parameters.
- A function can return a value using the return keyword.
- Functions are executed only when they are called.
