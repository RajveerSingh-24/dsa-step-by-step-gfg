# Palindrome Number

## Problem

Given an integer `N`, determine whether it is a **palindrome**.

A palindrome number reads the same forward and backward.

## Approach

- Store the original number.
- Reverse the digits of the number.
- Compare the reversed number with the original.
- If both are equal, the number is a palindrome.

## Code (Java)

```java
class Solution {
    static boolean isPalindrome(int n) {
        int original = n;
        int reversed = 0;

        while (n > 0) {
            int digit = n % 10;
            reversed = reversed * 10 + digit;
            n /= 10;
        }

        return original == reversed;
    }
}
```

## Example

Input:

```text
N = 121
```

Output:

```text
true
```

Explanation:

```text
Reverse of 121 is 121, so it is a palindrome.
```

## Complexity Analysis

- **Time Complexity:** O(log₁₀N)
- **Space Complexity:** O(1)

## Concept Used

- Digit Manipulation
- Number Reversal
- While Loop
- Modulus Operator (`%`)
