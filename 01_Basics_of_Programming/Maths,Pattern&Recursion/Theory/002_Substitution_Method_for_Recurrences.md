# Substitution Method for Recurrences

## What is Substitution Method?

The **Substitution Method** is a technique used to solve recurrence relations by repeatedly expanding the recurrence and finding a pattern.

It helps in predicting the time complexity of recursive algorithms.

## Steps of Substitution Method

1. Expand the recurrence by replacing smaller subproblems.
2. Continue expanding until the base case is reached.
3. Identify the pattern formed.
4. Use mathematical induction to prove the solution.

## Example

Given recurrence:
```
T(n) = T(n/2) + n
```
Expanding:
```
T(n) = T(n/4) + n/2 + n
T(n) = T(n/8) + n/4 + n/2 + n
```
Pattern:
```
T(n) = n + n/2 + n/4 + ... + 1
```
This is a geometric series:
```
T(n) = O(n)
```

## Advantages

- Simple and intuitive approach.
- Helps understand the behavior of recursive algorithms.
- Useful for verifying solutions obtained using other methods.

## Disadvantages

- Expansion can become complicated for complex recurrences.
- Requires guessing the correct solution before proving it.

## Applications

- Analyzing divide-and-conquer algorithms.
- Finding time complexity of recursive functions.
- Used in algorithms like Merge Sort and Binary Search.
