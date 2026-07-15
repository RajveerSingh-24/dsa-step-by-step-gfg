# Solid Rectangle

## Problem

Print a **solid rectangle** consisting of `*` (asterisks) with `N` rows and `M` columns.

## Example
Input:
```
N = 3
M = 5
```

Output:
```
* * * * *
* * * * *
* * * * *
```
## Approach

- Use two nested loops.
- The outer loop runs for each row.
- The inner loop prints `M` asterisks in each row.
- After printing a row, move to the next line.

## Code (Java)

```java
class Solution {
    static void printRectangle(int n, int m) {
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```
