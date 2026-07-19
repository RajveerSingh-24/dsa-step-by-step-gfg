# All Divisors of a Number

## Problem

Given a positive integer `N`, print all of its divisors in **ascending order**.

A divisor is a number that divides `N` exactly without leaving a remainder.

## Approach

- Iterate from `1` to `√N`.
- If `i` divides `N`, then both `i` and `N / i` are divisors.
- Store the divisors in a list.
- Print them in ascending order.

## Code (Java)

```java
import java.util.ArrayList;
import java.util.Collections;

class Solution {
    static ArrayList<Integer> divisors(int n) {
        ArrayList<Integer> list = new ArrayList<>();

        for (int i = 1; i * i <= n; i++) {
            if (n % i == 0) {
                list.add(i);

                if (i != n / i) {
                    list.add(n / i);
                }
            }
        }

        Collections.sort(list);
        return list;
    }
}
```

## Example

Input:

```text
N = 12
```

Output:

```text
1 2 3 4 6 12
```

Explanation:

```text
The numbers that divide 12 exactly are:
1, 2, 3, 4, 6, and 12.
```

## Complexity Analysis

- **Time Complexity:** O(√N + D log D), where `D` is the number of divisors (sorting the list).
- **Space Complexity:** O(D)

## Concept Used

- Factors
- Square Root Optimization
- ArrayList
- Sorting
- Modulus Operator (`%`)
