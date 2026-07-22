# Majority Element (More Than N/3 Times)

## Problem

Given an array of size `N`, find all elements that appear **more than ⌊N/3⌋ times**.

There can be **at most two** such elements.

## Approach

- Use the **Extended Moore's Voting Algorithm**.
- Maintain two candidates and their counts.
- Traverse the array to identify potential candidates.
- Traverse the array again to verify their frequencies.
- Return the candidates that occur more than `N / 3` times.

## Code (Java)

```java
import java.util.ArrayList;
import java.util.List;

class Solution {
    static List<Integer> majorityElement(int[] nums) {
        int candidate1 = 0, candidate2 = 0;
        int count1 = 0, count2 = 0;

        // Find potential candidates
        for (int num : nums) {
            if (candidate1 == num) {
                count1++;
            } else if (candidate2 == num) {
                count2++;
            } else if (count1 == 0) {
                candidate1 = num;
                count1 = 1;
            } else if (count2 == 0) {
                candidate2 = num;
                count2 = 1;
            } else {
                count1--;
                count2--;
            }
        }

        // Verify candidates
        count1 = 0;
        count2 = 0;

        for (int num : nums) {
            if (num == candidate1) {
                count1++;
            } else if (num == candidate2) {
                count2++;
            }
        }

        List<Integer> result = new ArrayList<>();

        if (count1 > nums.length / 3) {
            result.add(candidate1);
        }

        if (count2 > nums.length / 3) {
            result.add(candidate2);
        }

        return result;
    }
}
```

## Example

Input:

```text
nums = [3, 2, 3]
```

Output:

```text
[3]
```

### Another Example

Input:

```text
nums = [1, 1, 1, 3, 3, 2, 2, 2]
```

Output:

```text
[1, 2]
```

## Explanation

```text
At most two elements can appear
more than ⌊N/3⌋ times in an array.
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Extended Moore's Voting Algorithm
- Candidate Selection
- Frequency Verification
