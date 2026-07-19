# Check if an Array is Sorted

## Problem

Given an array of integers, determine whether the array is sorted in **non-decreasing order**.

## Approach

- Traverse the array from the second element.
- Compare each element with its previous element.
- If any element is smaller than its previous element, the array is not sorted.
- If no such pair is found, the array is sorted.

## Code (Java)

```java
class Solution {
    static boolean arraySortedOrNot(int[] arr) {
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < arr[i - 1]) {
                return false;
            }
        }
        return true;
    }
}
```

## Example

Input:

```text
arr = [1, 2, 2, 4, 5]
```

Output:

```text
true
```

Explanation:

```text
Each element is greater than or equal to its previous element, so the array is sorted.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Linear Traversal
- Comparison
- Conditional Statements
