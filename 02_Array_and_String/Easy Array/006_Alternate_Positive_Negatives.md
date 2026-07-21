# Rearrange Array in Alternate Positive and Negative Order

## Problem

Given an array containing positive and negative integers, rearrange the elements so that positive and negative numbers appear alternately while maintaining their relative order whenever possible.

## Approach

- Store positive and negative elements in separate lists.
- Traverse both lists simultaneously.
- Place one positive element followed by one negative element.
- Append any remaining elements after one list is exhausted.

## Code (Java)

```java
import java.util.ArrayList;

class Solution {
    static int[] rearrange(int[] arr) {
        ArrayList<Integer> positive = new ArrayList<>();
        ArrayList<Integer> negative = new ArrayList<>();

        for (int num : arr) {
            if (num >= 0) {
                positive.add(num);
            } else {
                negative.add(num);
            }
        }

        int[] result = new int[arr.length];
        int i = 0, p = 0, n = 0;

        while (p < positive.size() && n < negative.size()) {
            result[i++] = positive.get(p++);
            result[i++] = negative.get(n++);
        }

        while (p < positive.size()) {
            result[i++] = positive.get(p++);
        }

        while (n < negative.size()) {
            result[i++] = negative.get(n++);
        }

        return result;
    }
}
```

## Example

Input:

```text
arr = [1, 2, -3, -4, 5, -6]
```

Output:

```text
[1, -3, 2, -4, 5, -6]
```

## Explanation

```text
Positive and negative numbers are placed alternately.
If one type has extra elements, they are added at the end.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(N)

## Concept Used

- Arrays
- ArrayList
- Traversal
- Rearrangement
