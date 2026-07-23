# Sorted Subarray of Size 3

## Problem

Given an array, determine whether there exists a **sorted subarray of size 3**.

A sorted subarray of size 3 consists of three consecutive elements such that:

```text
arr[i] < arr[i + 1] < arr[i + 2]
```

## Approach

- Traverse the array from index `0` to `N - 3`.
- For each index, check whether the current element, the next element, and the following element are in strictly increasing order.
- If such a triplet is found, return `true`.
- Otherwise, return `false`.

## Code (Java)

```java
class Solution {
    static boolean hasSortedSubarray(int[] arr) {
        for (int i = 0; i <= arr.length - 3; i++) {
            if (arr[i] < arr[i + 1] &&
                arr[i + 1] < arr[i + 2]) {
                return true;
            }
        }

        return false;
    }
}
```

## Example

Input:

```text
arr = [5, 1, 2, 3, 4]
```

Output:

```text
true
```

### Another Example

Input:

```text
arr = [5, 4, 3, 2, 1]
```

Output:

```text
false
```

## Explanation

```text
The subarray [1, 2, 3] is sorted in
strictly increasing order, so the answer is true.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Linear Traversal
- Consecutive Element Comparison
- Conditional Statements
