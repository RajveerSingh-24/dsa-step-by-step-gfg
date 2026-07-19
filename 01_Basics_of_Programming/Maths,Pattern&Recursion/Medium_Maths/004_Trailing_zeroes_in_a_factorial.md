# Trailing Zeros in a Factorial

## Problem

Given an integer `N`, find the number of trailing zeros in `N!` (factorial of `N`).

Trailing zeros are the consecutive zeros at the end of the factorial.

## Approach

- A trailing zero is formed by the pair `2 × 5`.
- Since factors of `2` are more frequent than factors of `5`, count only the number of factors of `5`.
- Add the count of multiples of `5`, `25`, `125`, and so on until the divisor exceeds `N`.

## Code (Java)

```java
class Solution {
    static int trailingZeroes(int n) {
        int count = 0;

        while (n >= 5) {
            n /= 5;
            count += n;
        }

        return count;
    }
}
```

## Example

Input:

```text
N = 10
```

Output:

```text
2
```

Explanation:

```text
10! = 3628800

There are 2 trailing zeros.
```

## Complexity Analysis

- **Time Complexity:** O(log₅N)
- **Space Complexity:** O(1)

## Concept Used

- Factorial
- Prime Factorization
- Mathematical Counting
- While Loop
