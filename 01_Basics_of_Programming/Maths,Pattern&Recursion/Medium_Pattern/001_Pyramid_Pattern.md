# Pyramid Pattern

## Problem

Print a **pyramid pattern** of `N` rows using `*` (asterisks).

## Approach

- Use the outer loop to iterate through each row.
- Print `(N - i)` spaces before the stars.
- Print `(2 × i - 1)` stars in each row.
- Move to the next line after printing each row.

## Code (Java)

```java
class Solution {
    static void printPyramid(int n) {
        for (int i = 1; i <= n; i++) {

            // Print leading spaces
            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }

            // Print stars
            for (int j = 1; j <= (2 * i - 1); j++) {
                System.out.print("*");
            }

            System.out.println();
        }
    }
}
```

## Example

Input:

```text
N = 5
```

Output:

```text
    *
   ***
  *****
 *******
*********
```

## Complexity Analysis

- **Time Complexity:** O(N²)
- **Space Complexity:** O(1)

## Concept Used

- Nested Loops
- Pattern Printing
- Space and Character Manipulation
