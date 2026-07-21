# Stock Buy and Sell (Multiple Transactions Allowed)

## Problem

Given an array where each element represents the stock price on a particular day, find the **maximum profit** that can be earned by making **multiple buy and sell transactions**.

> You may complete as many transactions as you like, but you must sell the stock before buying again.

## Approach

- Traverse the array once.
- Whenever today's price is greater than yesterday's price, add the difference to the profit.
- This captures every profitable upward movement.

## Code (Java)

```java
class Solution {
    static int maxProfit(int[] prices) {
        int profit = 0;

        for (int i = 1; i < prices.length; i++) {
            if (prices[i] > prices[i - 1]) {
                profit += prices[i] - prices[i - 1];
            }
        }

        return profit;
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
7
```

## Explanation

```text
Buy at 1, Sell at 5 → Profit = 4
Buy at 3, Sell at 6 → Profit = 3

Total Profit = 4 + 3 = 7
```

## Complexity Analysis

- **Time Complexity:** O(N)
- **Space Complexity:** O(1)

## Concept Used

- Arrays
- Greedy Algorithm
- Single Traversal
- Profit Accumulation
