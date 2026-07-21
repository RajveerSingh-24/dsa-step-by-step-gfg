# Array Leaders

## Problem

Given an array, find all **leader** elements.

A leader is an element that is **greater than or equal to all the elements to its right**. The rightmost element is always a leader.

## Approach

- Traverse the array from **right to left**.
- Keep track of the maximum element seen so far.
- If the current element is greater than or equal to the maximum, it is a leader.
- Store the leaders and reverse the result to maintain the original order.

## Code (Java)

```java
import java.util.ArrayList;
import java.util.Collections;

class Solution {
    static ArrayList<Integer> leaders(int[] arr) {
        ArrayList<Integer> result = new ArrayList<>();
        int max = arr[arr.length - 1];

        result.add(max);

        for (int i = arr.length - 2; i >= 0; i--) {
            if (arr[i] >= max) {
                max = arr[i];
                result.add(max);
            }
        }

        Collections.reverse(result);
        return result;
    }
}
```

## Example

Input:

```text
arr = [16, 17, 4, 3, 5, 2]
```

Output:

```text
[17, 5, 2]
```

## Explanation

```text
17 is greater than all elements to its right.
5 is greater than 2.
2 is the last element, so it is always a leader.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Concept Used

- Arrays
- Reverse Traversal
- Maximum Element Tracking
- ArrayList
```
