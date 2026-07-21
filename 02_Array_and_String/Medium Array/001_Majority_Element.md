# Majority Element

## Problem

Given an array of size `N`, find the **majority element**.

A majority element is an element that appears **more than ⌊N/2⌋ times** in the array. If no such element exists, return `-1`.

## Approach

- Use **Moore's Voting Algorithm**.
- Traverse the array to find a potential majority candidate.
- Traverse the array again to verify whether the candidate appears more than `N / 2` times.
- Return the candidate if it is a valid majority element; otherwise, return `-1`.

## Code (Java)

```java
class Solution {
    static int majorityElement(int[] arr) {
        int candidate = 0;
        int count = 0;

        // Find potential candidate
        for (int num : arr) {
            if (count == 0) {
                candidate = num;
            }

            if (num == candidate) {
                count++;
            } else {
                count--;
            }
        }

        // Verify candidate
        count = 0;
        for (int num : arr) {
            if (num == candidate) {
                count++;
            }
        }

        return (count > arr.length / 2) ? candidate : -1;
    }
}
```

## Example

Input:

```text
arr = [2, 2, 1, 1, 2, 2, 2]
```

Output:

```text
2
```

### Another Example

Input:

```text
arr = [1, 2, 3, 4]
```

Output:

```text
-1
```

## Explanation

```text
The majority element appears more than
⌊N/2⌋ times in the array.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Moore's Voting Algorithm
- Candidate Selection
- Frequency Verification
