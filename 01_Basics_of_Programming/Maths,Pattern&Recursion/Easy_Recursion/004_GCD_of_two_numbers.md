# GCD of Two Numbers

## Problem

Given two positive integers `A` and `B`, find their **Greatest Common Divisor (GCD)**.

The GCD is the largest positive integer that divides both numbers without leaving a remainder.

## Approach

- Use **Euclid's Algorithm**.
- If `B` becomes `0`, then `A` is the GCD.
- Otherwise, recursively find the GCD of `B` and `A % B`.

## Code (Java)

```java
class Solution {
    static int gcd(int a, int b) {
        if (b == 0) {
            return a;
        }

        return gcd(b, a % b);
    }
}
```

## Example

Input:

```text
A = 24
B = 36
```

Output:

```text
12
```

Explanation:

```text
The largest number that divides both 24 and 36 is 12.
```

## Complexity Analysis

- **Time Complexity:** O(log(min(A, B)))
- **Space Complexity:** O(log(min(A, B))) (Recursion Stack)

## Concept Used

- Euclid's Algorithm
- Recursion
- Modulus Operator (`%`)
