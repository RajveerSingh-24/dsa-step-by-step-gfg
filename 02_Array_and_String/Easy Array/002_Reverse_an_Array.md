# Reverse an Array

## Problem

Given an array, reverse its elements **in place**.

## Approach

- Use two pointers:
  - One at the beginning of the array.
  - One at the end of the array.
- Swap the elements at both pointers.
- Move the left pointer forward and the right pointer backward.
- Continue until both pointers meet.

## Code (Java)

```java
class Solution {
    static void reverseArray(int[] arr) {
        int left = 0;
        int right = arr.length - 1;

        while (left < right) {
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;

            left++;
            right--;
        }
    }
}
```

## Example

Input:

```text
arr = [1, 2, 3, 4, 5]
```

Output:

```text
[5, 4, 3, 2, 1]
```

Explanation:

```text
The first and last elements are swapped repeatedly until the array is completely reversed.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Two-Pointer Technique
- Swapping
- In-Place Modification
