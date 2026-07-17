# Prime Number

## Problem

Given an integer `N`, determine whether it is a **prime number**.

A prime number is a number greater than `1` that has exactly two factors: `1` and itself.

## Approach

- If `N` is less than or equal to `1`, it is not prime.
- Check for divisors from `2` to `√N`.
- If any number divides `N` exactly, it is not prime.
- Otherwise, it is prime.

## Code (Java)

```java
class Solution {
    static boolean isPrime(int n) {
        if (n <= 1) {
            return false;
        }

        for (int i = 2; i * i <= n; i++) {
            if (n % i == 0) {
                return false;
            }
        }

        return true;
    }
}
```

## Example

Input:

```text
N = 29
```

Output:

```text
Prime
```

Explanation:

```text
29 has only two factors: 1 and 29.
```

## Complexity Analysis

- **Time Complexity:** O(√N)
- **Space Complexity:** O(1)

## Concept Used

- Prime Numbers
- Factor Checking
- Square Root Optimization
- Modulus Operator (`%`)
