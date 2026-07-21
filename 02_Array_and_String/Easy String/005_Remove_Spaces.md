# Remove Spaces from a String

## Problem

Given a string, remove **all spaces** from it and return the modified string.

## Approach

- Traverse each character of the string.
- If the character is **not a space (' ')**, append it to a `StringBuilder`.
- Return the resulting string.

## Code (Java)

```java
class Solution {
    static String removeSpaces(String str) {
        StringBuilder result = new StringBuilder();

        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) != ' ') {
                result.append(str.charAt(i));
            }
        }

        return result.toString();
    }
}
```

## Example

Input:

```text
str = "Geeks for Geeks"
```

Output:

```text
GeeksforGeeks
```

## Explanation

```text
All space characters are removed,
while the remaining characters stay unchanged.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Concept Used

- Strings
- Character Comparison
- StringBuilder
- Traversal
