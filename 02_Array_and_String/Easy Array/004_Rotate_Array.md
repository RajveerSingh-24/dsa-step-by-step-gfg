# Rotate Array

## Problem

Given an array and an integer `K`, rotate the array to the **left** by `K` positions.

## Approach

- Compute `K % N` to handle rotations greater than the array size.
- Reverse the first `K` elements.
- Reverse the remaining `N - K` elements.
- Reverse the entire array.
- The array is now rotated to the left.

## Code (Java)

```java
class Solution {

    static void reverse(int[] arr, int left, int right) {
        while (left < right) {
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;

            left++;
            right--;
        }
    }

    static void rotateLeft(int[] arr, int k) {
        int n = arr.length;
        k %= n;

        reverse(arr, 0, k - 1);
        reverse(arr, k, n - 1);
        reverse(arr, 0, n - 1);
    }
}
```

## Example

Input:

```text
arr = [1, 2, 3, 4, 5]
K = 2
```

Output:

```text
[3, 4, 5, 1, 2]
```

Explanation:

```text
After rotating the array left by 2 positions,
the first two elements move to the end.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Array Reversal
- Two-Pointer Technique
- In-Place Rotation
