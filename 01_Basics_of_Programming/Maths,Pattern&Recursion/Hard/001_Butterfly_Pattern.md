# Butterfly Pattern

## Problem

Print a **Butterfly Pattern** of size `N` using `*` (asterisks).

The pattern consists of:
- An upper half
- A lower half
- Stars on both sides
- Spaces in the middle

## Approach

- Use nested loops.
- In the upper half:
  - Print increasing stars.
  - Print decreasing spaces.
  - Print increasing stars again.
- In the lower half:
  - Print decreasing stars.
  - Print increasing spaces.
  - Print decreasing stars again.

## Code (Java)

```java
class Solution {
    static void printButterfly(int n) {

        // Upper Half
        for (int i = 1; i <= n; i++) {

            // Left stars
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }

            // Middle spaces
            for (int j = 1; j <= 2 * (n - i); j++) {
                System.out.print(" ");
            }

            // Right stars
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }

            System.out.println();
        }

        // Lower Half
        for (int i = n; i >= 1; i--) {

            // Left stars
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }

            // Middle spaces
            for (int j = 1; j <= 2 * (n - i); j++) {
                System.out.print(" ");
            }

            // Right stars
            for (int j = 1; j <= i; j++) {
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
N = 4
```

Output:

```text
*      *
**    **
***  ***
********
********
***  ***
**    **
*      *
```

## Complexity Analysis

- **Time Complexity:** O(N²)
- **Space Complexity:** O(1)

## Concept Used

- Nested Loops
- Pattern Printing
- Space Manipulation
- Symmetry
