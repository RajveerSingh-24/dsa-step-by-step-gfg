# Introduction to Recursion

## What is Recursion?

Recursion is a programming technique where a function calls itself to solve a smaller version of the same problem.

A recursive function has two main parts:

1. **Base Case** - The condition that stops the recursion.
2. **Recursive Case** - The part where the function calls itself with a smaller input.

## How Recursion Works

Each recursive call is stored in the **call stack** until the base case is reached. Then the functions return their results in reverse order.

## Example: Print Numbers Using Recursion (Java)

```java
public class RecursionExample {

    static void printNumbers(int n) {
        // Base Case
        if (n == 0) {
            return;
        }

        // Recursive Case
        System.out.println(n);
        printNumbers(n - 1);
    }

    public static void main(String[] args) {
        printNumbers(5);
    }
}  
```
Output:
```
5
4
3
2
1
```
---
## Example: Factorial Using Recursion
```java
public class Factorial {

    static int factorial(int n) {
        // Base Case
        if (n == 0 || n == 1) {
            return 1;
        }

        // Recursive Case
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        System.out.println(factorial(5));
    }
}
```
Output:
```
120
```
---
## Advantages of Recursion
- Makes code shorter and easier to understand.
- Useful for problems that can be divided into smaller subproblems.
- Commonly used in tree traversal, graphs, backtracking, and divide-and-conquer algorithms.

## Disadvantages of Recursion
- Uses extra memory due to the call stack.
- Can cause StackOverflowError if the base case is missing.
- Sometimes iterative solutions are more efficient.
