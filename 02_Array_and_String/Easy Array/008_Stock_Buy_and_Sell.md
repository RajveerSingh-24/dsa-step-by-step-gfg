# Stock Buy and Sell (Maximum One Transaction)

## Problem

Given an array where each element represents the stock price on a particular day, find the **maximum profit** that can be earned by making **at most one buy and one sell**.

> You must buy before you sell.

## Approach

- Traverse the array once.
- Keep track of the **minimum price** seen so far.
- For each day's price:
  - Calculate the profit by selling on that day.
  - Update the maximum profit if the current profit is higher.
- Update the minimum price whenever a lower price is found.

## Code (Java)

```java
class Solution {
    static int maxProfit(int[] prices) {
        int minPrice = Integer.MAX_VALUE;
        int maxProfit = 0;

        for (int price : prices) {
            minPrice = Math.min(minPrice, price);
            maxProfit = Math.max(maxProfit, price - minPrice);
        }

        return maxProfit;
    }
}
```

## Example

Input:

```text
prices = [7, 1, 5, 3, 6, 4]
```

Output:

```text
5
```

## Explanation

```text
Buy at price 1 (Day 2)
Sell at price 6 (Day 5)

Profit = 6 - 1 = 5
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Greedy Algorithm
- Minimum Element Tracking
- Single Traversal
