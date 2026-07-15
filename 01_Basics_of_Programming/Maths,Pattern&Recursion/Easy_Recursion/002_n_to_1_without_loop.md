# Print N to 1 Without Loop

## Problem

Print numbers from `N` to `1` without using any loop.

## Approach

- Use **recursion** instead of loops.
- Print the current number first.
- Recursively call the function with `N - 1`.
- Stop when `N` becomes `0`.

## Code (Java)

```java
class Solution {
    static void printNos(int n) {
        if (n == 0) {
            return;
        }

        System.out.print(n + " ");
        printNos(n - 1);
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
5 4 3 2 1
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N) (Recursion Stack)

## Concept Used

- Recursion
- Base Case
- Recursive Function Calls
