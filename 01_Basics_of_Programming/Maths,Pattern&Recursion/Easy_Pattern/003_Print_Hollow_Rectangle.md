# Print Hollow Rectangle

## Problem

Print a **hollow rectangle** of `N` rows and `M` columns using `*` (asterisks). Only the boundary should contain `*`, while the inside should contain spaces.

## Approach

- Use two nested loops to traverse each row and column.
- Print `*` if the current position is on the boundary:
  - First row
  - Last row
  - First column
  - Last column
- Otherwise, print a space.

## Code (Java)

```java
class Solution {
    static void printHollowRectangle(int n, int m) {
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= m; j++) {
                if (i == 1 || i == n || j == 1 || j == m) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
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
M = 5
```

Output:

```text
* * * * *
*       *
*       *
* * * * *
```

## Complexity Analysis

- **Time Complexity:** O(N × M)
- **Space Complexity:** O(1)

## Concept Used

- Nested Loops
- Pattern Printing
- Conditional Statements
