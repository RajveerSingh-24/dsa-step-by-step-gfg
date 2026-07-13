# Prime Number (Java)

## Problem Statement
Given a number `N`, check whether it is a **prime number** or not.

A prime number is a number greater than 1 that has exactly two factors:
- 1
- The number itself

Examples:
- 2, 3, 5, 7 are prime numbers.
- 4, 6, 8, 9 are not prime numbers.

## Approach
- If `n <= 1`, it is not prime.
- Check divisibility from `2` to `√n`.
- If any number divides `n`, then it is not prime.
- Otherwise, the number is prime.

## Java Code

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
