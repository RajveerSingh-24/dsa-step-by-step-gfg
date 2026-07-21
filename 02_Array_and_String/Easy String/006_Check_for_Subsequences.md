# Check for Subsequences

## Problem

Given two strings `S1` and `S2`, determine whether `S1` is a **subsequence** of `S2`.

A subsequence is formed by deleting zero or more characters from a string without changing the order of the remaining characters.

## Approach

- Use two pointers:
  - One for `S1`.
  - One for `S2`.
- Traverse `S2`.
- Whenever the characters match, move both pointers.
- Otherwise, move only the pointer of `S2`.
- If all characters of `S1` are matched, it is a subsequence.

## Code (Java)

```java
class Solution {
    static boolean isSubsequence(String s1, String s2) {
        int i = 0;
        int j = 0;

        while (i < s1.length() && j < s2.length()) {
            if (s1.charAt(i) == s2.charAt(j)) {
                i++;
            }
            j++;
        }

        return i == s1.length();
    }
}
```

## Example

Input:

```text
S1 = "ace"
S2 = "abcde"
```

Output:

```text
true
```

### Another Example

Input:

```text
S1 = "aec"
S2 = "abcde"
```

Output:

```text
false
```

## Explanation

```text
The characters of a subsequence must appear
in the same relative order, but not necessarily consecutively.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

Where `N` is the length of `S2`.

## Concept Used

- Strings
- Two-Pointer Technique
- Character Comparison
- Traversal
