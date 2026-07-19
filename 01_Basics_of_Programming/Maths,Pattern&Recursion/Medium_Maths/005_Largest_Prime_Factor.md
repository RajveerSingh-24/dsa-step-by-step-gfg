# Largest Prime Factor

## Problem

Given a positive integer `N`, find its **largest prime factor**.

A prime factor is a factor of a number that is also a prime number.

## Approach

- Divide `N` by `2` until it is no longer divisible.
- Check odd numbers from `3` up to `√N`.
- Whenever a divisor is found, divide `N` completely by that divisor and update the largest prime factor.
- If the remaining `N` is greater than `2`, it is also a prime factor and is the largest.

## Code (Java)

```java
class Solution {
    static long largestPrimeFactor(long n) {
        long largest = -1;

        while (n % 2 == 0) {
            largest = 2;
            n /= 2;
        }

        for (long i = 3; i * i <= n; i += 2) {
            while (n % i == 0) {
                largest = i;
                n /= i;
            }
        }

        if (n > 2) {
            largest = n;
        }

        return largest;
    }
}
```

## Example

Input:

```text
N = 315
```

Output:

```text
7
```

Explanation:

```text
315 = 3 × 3 × 5 × 7

The largest prime factor is 7.
```

## Complexity Analysis

- **Time Complexity:** O(√N)
- **Space Complexity:** O(1)

## Concept Used

- Prime Factorization
- Square Root Optimization
- While Loop
- Modulus Operator (`%`)
