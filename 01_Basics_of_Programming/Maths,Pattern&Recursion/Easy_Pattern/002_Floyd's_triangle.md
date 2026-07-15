# Floyd's Triangle

## Problem

Print **Floyd's Triangle** for a given number of rows `N`.

In Floyd's Triangle, consecutive natural numbers are printed in a triangular pattern.

## Example

Input:

```text
N = 5
```

Output:

```text
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

## Approach

- Initialize a variable `num = 1`.
- Use the outer loop to iterate through each row.
- Use the inner loop to print the required numbers in the current row.
- Increment `num` after printing each number.

## Code (Java)

```java
class Solution {
    static void printFloydTriangle(int n) {
        int num = 1;

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(num + " ");
                num++;
            }
            System.out.println();
        }
    }
}
```



## Complexity Analysis

- **Time Complexity:** O(N²)
- **Space Complexity:** O(1)

## Concept Used

- Nested Loops
- Pattern Printing
- Increment Operator
