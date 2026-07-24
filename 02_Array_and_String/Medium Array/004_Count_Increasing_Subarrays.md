# Count Increasing Subarrays

## Problem

Given an array, count the total number of **strictly increasing contiguous subarrays** of length greater than `1`.

An increasing subarray is one in which every element is greater than its previous element.

## Approach

- Traverse the array once.
- Maintain the length of the current increasing sequence.
- If the current element is greater than the previous one, extend the sequence.
- Otherwise, calculate the number of increasing subarrays formed by the previous sequence using:

```text
count = length × (length - 1) / 2
```

- Repeat the process for the last sequence.

## Code (Java)

```java
class Solution {
    static int countIncreasingSubarrays(int[] arr) {
        int n = arr.length;
        int length = 1;
        int count = 0;

        for (int i = 1; i < n; i++) {
            if (arr[i] > arr[i - 1]) {
                length++;
            } else {
                count += (length * (length - 1)) / 2;
                length = 1;
            }
        }

        count += (length * (length - 1)) / 2;

        return count;
    }
}
```

## Example

Input:

```text
arr = [1, 2, 3, 4]
```

Output:

```text
6
```

## Explanation

```text
Increasing subarrays are:

[1,2]
[2,3]
[3,4]
[1,2,3]
[2,3,4]
[1,2,3,4]

Total = 6
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Linear Traversal
- Counting
- Increasing Sequences
