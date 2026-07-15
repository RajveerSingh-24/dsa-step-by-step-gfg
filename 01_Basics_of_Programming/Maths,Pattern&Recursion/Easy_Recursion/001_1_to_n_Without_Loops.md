# Print 1 to N Without Loop

## Problem

Print numbers from `1` to `N` without using any loop.

## Approach

- Use **recursion** instead of loops.
- Recursively call the function for `N - 1`.
- Print the current number while returning from the recursive calls.

## Code (Java)

```java
class Solution {
    static void printNos(int n) {
        if (n == 0) {
            return;
        }

        printNos(n - 1);
        System.out.print(n + " ");
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
1 2 3 4 5
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N) (Recursion Stack)

## Concept Used

- Recursion
- Base Case
- Recursive Function Calls
