# Hollow Diamond Pattern

## Problem

Print a **hollow diamond** pattern of `N` rows (upper half) using `*` (asterisks).

## Approach

- The pattern consists of two halves:
  - Upper half
  - Lower half
- Print leading spaces for alignment.
- Print `*` only at the boundary of each row.
- Fill the inside with spaces to create the hollow effect.

## Code (Java)

```java
class Solution {
    static void printHollowDiamond(int n) {

        // Upper Half
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n - i; j++)
                System.out.print(" ");

            for (int j = 1; j <= 2 * i - 1; j++) {
                if (j == 1 || j == 2 * i - 1)
                    System.out.print("*");
                else
                    System.out.print(" ");
            }
            System.out.println();
        }

        // Lower Half
        for (int i = n - 1; i >= 1; i--) {
            for (int j = 1; j <= n - i; j++)
                System.out.print(" ");

            for (int j = 1; j <= 2 * i - 1; j++) {
                if (j == 1 || j == 2 * i - 1)
                    System.out.print("*");
                else
                    System.out.print(" ");
            }
            System.out.println();
        }
    }
}
```

## Example

Input:

```text
N = 4
```

Output:

```text
   *
  * *
 *   *
*     *
 *   *
  * *
   *
```

## Complexity Analysis

- **Time Complexity:** O(N²)
- **Space Complexity:** O(1)

## Concept Used

- Nested Loops
- Pattern Printing
- Conditional Statements
- Space Manipulation
