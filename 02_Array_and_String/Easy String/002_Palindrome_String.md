# Palindrome String

## Problem

Given a string, determine whether it is a **palindrome**.

A palindrome string reads the same forward and backward.

## Approach

- Use two pointers:
  - One at the beginning of the string.
  - One at the end of the string.
- Compare the characters at both pointers.
- If they differ, the string is not a palindrome.
- Move both pointers toward the center until they meet.

## Code (Java)

```java
class Solution {
    static boolean isPalindrome(String str) {
        int left = 0;
        int right = str.length() - 1;

        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false;
            }

            left++;
            right--;
        }

        return true;
    }
}
```

## Example

Input:

```text
str = "madam"
```

Output:

```text
true
```

### Another Example

Input:

```text
str = "hello"
```

Output:

```text
false
```

## Explanation

```text
A palindrome has the same sequence of characters
when read from left to right and right to left.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Strings
- Two-Pointer Technique
- Character Comparison
