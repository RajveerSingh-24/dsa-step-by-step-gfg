# Toggle Case of a String

## Problem

Given a string, convert all **uppercase** letters to **lowercase** and all **lowercase** letters to **uppercase**.

## Approach

- Traverse each character of the string.
- If the character is uppercase, convert it to lowercase.
- If the character is lowercase, convert it to uppercase.
- Append the converted character to a `StringBuilder`.

## Code (Java)

```java
class Solution {
    static String toggleCase(String str) {
        StringBuilder result = new StringBuilder();

        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);

            if (Character.isUpperCase(ch)) {
                result.append(Character.toLowerCase(ch));
            } else if (Character.isLowerCase(ch)) {
                result.append(Character.toUpperCase(ch));
            } else {
                result.append(ch);
            }
        }

        return result.toString();
    }
}
```

## Example

Input:

```text
str = "HeLLo123"
```

Output:

```text
"hEllO123"
```

## Explanation

```text
Uppercase letters become lowercase,
lowercase letters become uppercase,
and non-alphabetic characters remain unchanged.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Concept Used

- Strings
- Character Manipulation
- `Character` Class
- `StringBuilder`
