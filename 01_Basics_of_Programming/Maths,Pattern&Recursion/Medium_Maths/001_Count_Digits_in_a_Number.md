# Count Total Digits in a Number

## Problem

Given an integer `N`, count the total number of digits present in it.

## Approach

- Initialize a counter to `0`.
- Repeatedly divide the number by `10`.
- Increment the counter after each division.
- Continue until the number becomes `0`.
- If `N` is `0`, the answer is `1`.

## Code (Java)

```java
class Solution {
    static int countDigits(int n) {
        if (n == 0) {
            return 1;
        }

        int count = 0;
        n = Math.abs(n);

        while (n > 0) {
            count++;
            n /= 10;
        }

        return count;
    }
}
```

## Example

Input:

```text
N = 12345
```

Output:

```text
5
```

Explanation:

```text
The number 12345 contains 5 digits.
```

## Complexity Analysis

- **Time Complexity:** O(log₁₀N)
- **Space Complexity:** O(1)

## Concept Used

- While Loop
- Integer Division
- Digit Manipulation
