# Two Water Jug Problem

## Problem

Given two jugs with capacities `M` and `N` liters and an unlimited water supply, determine whether it is possible to measure exactly `D` liters of water.

You can perform the following operations:
- Fill a jug completely.
- Empty a jug.
- Pour water from one jug to the other until one jug is either full or empty.

## Approach

- If `D` is greater than the larger jug's capacity, it is impossible.
- Otherwise, the measurement is possible if:
  - `D` is `0`, or
  - `D` is divisible by the **Greatest Common Divisor (GCD)** of `M` and `N`.

## Code (Java)

```java
class Solution {

    static int gcd(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }

    static boolean canMeasureWater(int m, int n, int d) {
        if (d > Math.max(m, n)) {
            return false;
        }

        if (d == 0) {
            return true;
        }

        return d % gcd(m, n) == 0;
    }

    public static void main(String[] args) {
        int m = 3, n = 5, d = 4;
        System.out.println(canMeasureWater(m, n, d));
    }
}
```

## Example

Input:

```text
M = 3
N = 5
D = 4
```

Output:

```text
true
```

Explanation:

```text
Fill the 5L jug and pour into the 3L jug.
Repeat the process until exactly 4L remains in the 5L jug.
```

## Complexity Analysis

- **Time Complexity:** O(log(min(M, N)))
- **Space Complexity:** O(1)

## Concept Used

- Euclid's Algorithm
- Greatest Common Divisor (GCD)
- Number Theory
- Mathematical Reasoning
