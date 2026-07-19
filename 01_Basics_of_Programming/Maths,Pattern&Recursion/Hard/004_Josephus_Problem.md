# Josephus Problem

## Problem

There are `N` people standing in a circle. Starting from the first person, every `K`-th person is eliminated until only one person remains.

Find the position of the last remaining person.

## Approach

- Use recursion to solve the problem for `N - 1` people.
- After each recursive call, adjust the survivor's position based on the elimination step `K`.
- The recursive relation is:

```
J(1, K) = 0
J(N, K) = (J(N - 1, K) + K) % N
```

- Convert the final answer to **1-based indexing** by adding `1`.

## Code (Java)

```java
class Solution {

    static int josephus(int n, int k) {
        if (n == 1) {
            return 1;
        }

        return (josephus(n - 1, k) + k - 1) % n + 1;
    }

    public static void main(String[] args) {
        int n = 7;
        int k = 3;
        System.out.println(josephus(n, k));
    }
}
```

## Example

Input:

```text
N = 7
K = 3
```

Output:

```text
4
```

Explanation:

```text
The elimination order is:
3 → 6 → 2 → 7 → 5 → 1

The last remaining person is at position 4.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N) (Recursion Stack)

## Concept Used

- Recursion
- Circular Indexing
- Modulus Operator (`%`)
