# First Non-Repeating Character

## Problem

Given a string, find the **first non-repeating character**.

A non-repeating character is one that appears exactly once in the string.

## Approach

- Use a frequency array of size `256` to count the occurrences of each character.
- Traverse the string once to build the frequency array.
- Traverse the string again and return the first character whose frequency is `1`.
- If no such character exists, return a special character (e.g., `'#'`).

## Code (Java)

```java
class Solution {
    static char firstNonRepeating(String str) {
        int[] freq = new int[256];

        for (int i = 0; i < str.length(); i++) {
            freq[str.charAt(i)]++;
        }

        for (int i = 0; i < str.length(); i++) {
            if (freq[str.charAt(i)] == 1) {
                return str.charAt(i);
            }
        }

        return '#';
    }
}
```

## Example

Input:

```text
str = "geeksforgeeks"
```

Output:

```text
f
```

### Another Example

Input:

```text
str = "aabbcc"
```

Output:

```text
#
```

## Explanation

```text
The first character that appears only once
is returned. If none exists, '#' is returned.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

> The frequency array has a fixed size (256), so the extra space is constant.

## Concept Used

- Strings
- Frequency Array
- Character Counting
- Traversal
