# Remove All Occurrences of a Character from a String

## Problem

Given a string and a character, remove **all occurrences** of the given character from the string.

## Approach

- Traverse each character of the string.
- If the current character is not equal to the given character, append it to a `StringBuilder`.
- Return the resulting string.

## Code (Java)

```java
class Solution {
    static String removeCharacter(String str, char ch) {
        StringBuilder result = new StringBuilder();

        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) != ch) {
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
str = "programming"
ch = 'm'
```

Output:

```text
prograing
```

## Explanation

```text
All occurrences of the character 'm'
are removed from the string.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Concept Used

- Strings
- Character Comparison
- StringBuilder
- Traversal
