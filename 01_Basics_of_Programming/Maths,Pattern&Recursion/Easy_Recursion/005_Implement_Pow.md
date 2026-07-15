# Implement Pow(x, n)

## Problem

Implement a function to calculate `x` raised to the power `n`, i.e., compute `xⁿ`.

## Approach

- Use **recursion with exponentiation by squaring**.
- If `n` is `0`, return `1`.
- If `n` is even, compute `pow(x, n/2)` once and square it.
- If `n` is odd, multiply `x` with `pow(x, n-1)`.

## Code (Java)

```java
class Solution {
    double power(double x, int n) {
        if (n == 0) {
            return 1;
        }

        if (n < 0) {
            return 1 / power(x, -n);
        }

        if (n % 2 == 0) {
            double half = power(x, n / 2);
            return half * half;
        }

        return x * power(x, n - 1);
    }
}
```

## Example

Input:

```text
x = 2
n = 10
```

Output:

```text
1024.0
```

Explanation:

```text
2¹⁰ = 1024
```

## Complexity Analysis

- **Time Complexity:** O(log n)
- **Space Complexity:** O(log n) (Recursion Stack)

## Concept Used

- Recursion
- Divide and Conquer
- Exponentiation by Squaring
