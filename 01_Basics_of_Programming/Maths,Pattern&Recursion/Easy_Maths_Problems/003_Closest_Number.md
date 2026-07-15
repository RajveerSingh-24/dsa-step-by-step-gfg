# Closest Number

## Problem

Given three integers `N`, `M`, and `K`, find the multiple of `M` that is closest to `N`. If two multiples are equally close, return the larger multiple.

## Example
Input:
```
N = 13
M = 4
```
Output:
```
12
```

## Approach

1. Find the quotient by dividing `N` by `M`.
2. Compute the two nearest multiples:
   - Lower multiple: `M × quotient`
   - Higher multiple: `M × (quotient + 1)`
3. Compare their distances from `N`.
4. If both are equally close, return the larger multiple.

## Code (Java)

```java
class Solution {
    static int closestNumber(int n, int m) {
        int q = n / m;

        int lower = m * q;
        int higher = (n * m > 0) ? m * (q + 1) : m * (q - 1);

        if (Math.abs(n - lower) < Math.abs(n - higher))
            return lower;
        else
            return higher;
    }
}
```
