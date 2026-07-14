# Recursion Tree Method to Solve Recurrences

## What is Recursion Tree Method?

The **Recursion Tree Method** is a technique used to solve recurrence relations by representing recursive calls as a tree structure.

Each node represents the cost of a subproblem, and the total cost is calculated by adding the costs at all levels of the tree.

## Steps of Recursion Tree Method

1. Draw the recursive calls as a tree.
2. Calculate the cost at each level.
3. Find the number of levels until the base case is reached.
4. Add the cost of all levels to find the final complexity.

## Example

Given recurrence:
```
T(n) = 2T(n/2) + n
```
Recursion Tree:
```
             n
          /     \
        n/2     n/2
       /  \     /  \
    n/4  n/4  n/4  n/4
```
Cost at each level:
```
Level 0: n
Level 1: 2 × n/2 = n
Level 2: 4 × n/4 = n
```
The cost remains the same at every level.
Number of levels:
```
log₂ n
```
Total cost:
```
T(n) = n × log₂ n
```
Therefore,
```
T(n) = O(n log n)
```

## Advantages

- Provides a visual understanding of recursive algorithms.
- Helps identify patterns in recurrence relations.
- Useful for divide-and-conquer algorithms.

## Disadvantages

- Can become complex for large or uneven recurrences.
- Requires careful calculation of each level.

## Applications

- Merge Sort analysis.
- Quick Sort analysis.
- Divide-and-conquer algorithms.
- Time complexity analysis of recursive programs.
