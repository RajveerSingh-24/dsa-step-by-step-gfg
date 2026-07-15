# Factorial of a Number

## Problem

Given a positive integer `N`, find its factorial.

The factorial of a number is the product of all positive integers from `1` to `N`.

```
Factorial(N) = N × (N - 1) × ... × 2 × 1
```

## Approach

- Use **recursion** to calculate the factorial.
- If `N` is `0` or `1`, return `1` (base case).
- Otherwise, return `N × factorial(N - 1)`.

## Code (Java)

```java
class Solution {
    static long factorial(int n) {
        if (n == 0 || n == 1) {
            return 1;
        }

        return n * factorial(n - 1);
    }
}
```

## Example

Input:

```text
N = 5
```

Output:

```text
120
```

Explanation:

```text
5 × 4 × 3 × 2 × 1 = 120
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N) (Recursion Stack)

## Concept Used

- Recursion
- Base Case
- Recursive Function Calls
