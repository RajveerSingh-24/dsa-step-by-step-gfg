# Odd or Even

## Problem

Given an integer `N`, determine whether the number is **odd** or **even**.

## Approach

A number is:
- **Even** if it is completely divisible by 2.
- **Odd** if it leaves a remainder when divided by 2.

We can use the modulus operator `%` to check the remainder.

## Code (Java)

```java
class Solution {
    static String oddEven(int N) {
        if (N % 2 == 0) {
            return "Even";
        } else {
            return "Odd";
        }
    }
}
