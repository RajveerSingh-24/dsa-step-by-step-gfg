# Reverse Array in Groups

## Problem

Given an array and an integer `K`, reverse the elements of the array in groups of size `K`.

If the remaining elements are fewer than `K`, reverse them as well.

## Approach

- Traverse the array in steps of `K`.
- For each group:
  - Set the left pointer to the start of the group.
  - Set the right pointer to the end of the group (or the last element of the array).
  - Reverse the group using the two-pointer technique.

## Code (Java)

```java
class Solution {
    static void reverseInGroups(int[] arr, int k) {
        int n = arr.length;

        for (int i = 0; i < n; i += k) {
            int left = i;
            int right = Math.min(i + k - 1, n - 1);

            while (left < right) {
                int temp = arr[left];
                arr[left] = arr[right];
                arr[right] = temp;

                left++;
                right--;
            }
        }
    }
}
```

## Example

Input:

```text
arr = [1, 2, 3, 4, 5, 6, 7, 8]
K = 3
```

Output:

```text
[3, 2, 1, 6, 5, 4, 8, 7]
```

Explanation:

```text
Group 1: [1, 2, 3] → [3, 2, 1]
Group 2: [4, 5, 6] → [6, 5, 4]
Group 3: [7, 8] → [8, 7]
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Two-Pointer Technique
- In-Place Reversal
- Traversal
