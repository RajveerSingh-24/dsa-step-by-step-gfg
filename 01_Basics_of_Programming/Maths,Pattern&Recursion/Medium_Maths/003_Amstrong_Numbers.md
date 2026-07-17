# Armstrong Number

## Problem

Given an integer `N`, determine whether it is an **Armstrong Number**.

An Armstrong number is a number that is equal to the sum of its digits, where each digit is raised to the power of the total number of digits.

## Approach

- Count the total number of digits in `N`.
- Traverse each digit of the number.
- Raise each digit to the power of the digit count and add it to a sum.
- If the sum equals the original number, it is an Armstrong number.

## Code (Java)

```java
class Solution {
    static boolean armstrongNumber(int n) {
        int original = n;
        int digits = String.valueOf(n).length();
        int sum = 0;

        while (n > 0) {
            int digit = n % 10;
            sum += Math.pow(digit, digits);
            n /= 10;
        }

        return sum == original;
    }
}
```

## Example

Input:

```text
N = 153
```

Output:

```text
true
```

Explanation:

```text
153 = 1³ + 5³ + 3³
    = 1 + 125 + 27
    = 153
```

## Complexity Analysis

- **Time Complexity:** O(d), where `d` is the number of digits.
- **Space Complexity:** O(1)

## Concept Used

- Digit Manipulation
- Mathematical Operations
- Armstrong Number
- `Math.pow()`
