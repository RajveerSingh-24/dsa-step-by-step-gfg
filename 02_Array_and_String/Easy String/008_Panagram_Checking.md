# Pangram Checking

## Problem

Given a string, determine whether it is a **pangram**.

A pangram is a sentence that contains **every letter of the English alphabet (a–z) at least once**, regardless of case.

## Approach

- Create a boolean array of size `26` to track the presence of each letter.
- Traverse the string:
  - Convert each character to lowercase.
  - If it is an alphabet, mark its corresponding index as `true`.
- Finally, check whether all 26 letters are present.

## Code (Java)

```java
class Solution {
    static boolean isPangram(String str) {
        boolean[] visited = new boolean[26];

        for (int i = 0; i < str.length(); i++) {
            char ch = Character.toLowerCase(str.charAt(i));

            if (ch >= 'a' && ch <= 'z') {
                visited[ch - 'a'] = true;
            }
        }

        for (boolean letter : visited) {
            if (!letter) {
                return false;
            }
        }

        return true;
    }
}
```

## Example

Input:

```text
str = "The quick brown fox jumps over the lazy dog"
```

Output:

```text
true
```

### Another Example

Input:

```text
str = "Hello World"
```

Output:

```text
false
```

## Explanation

```text
A pangram must contain every letter
from 'a' to 'z' at least once.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

> The boolean array always has a fixed size of 26.

## Concept Used

- Strings
- Boolean Array
- Character Manipulation
- Traversal
