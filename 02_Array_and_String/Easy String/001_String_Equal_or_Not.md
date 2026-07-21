# Check if Two Strings are Same

## Problem

Given two strings, determine whether they are **identical**.

Two strings are considered the same if they have the **same length** and **the same characters in the same order**.

## Approach

- Use the `equals()` method to compare both strings.
- If the strings are equal, return `true`.
- Otherwise, return `false`.

## Code (Java)

```java
class Solution {
    static boolean areSame(String str1, String str2) {
        return str1.equals(str2);
    }
}
```

## Example

Input:

```text
str1 = "hello"
str2 = "hello"
```

Output:

```text
true
```

### Another Example

Input:

```text
str1 = "Hello"
str2 = "hello"
```

Output:

```text
false
```

## Explanation

```text
String comparison using equals() is case-sensitive.
Both strings must have exactly the same characters.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Strings
- String Comparison
- `equals()` Method
