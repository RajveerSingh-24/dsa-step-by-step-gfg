# Master Theorem for Divide and Conquer Recurrences

## What is Master Theorem?

The **Master Theorem** is a method used to solve recurrence relations that occur in **divide-and-conquer algorithms**.

It helps find the time complexity without expanding the recurrence tree.

A common form of recurrence is:
```
T(n) = aT(n/b) + f(n)
```
Where:

- **a** = Number of subproblems created.
- **n/b** = Size of each subproblem.
- **f(n)** = Cost of dividing and combining the problem.

## Cases of Master Theorem

### Case 1

If:
```
f(n) = O(n^c)
```
where:
```
c < log_b(a)
```
Then:
```
T(n) = O(n^(log_b a))
```
Example:
```
T(n) = 2T(n/2) + 1

Result:
T(n) = O(n)
```

---

### Case 2

If:
```
f(n) = Θ(n^c)
```
where:
```
c = log_b(a)
```
Then:
```
T(n) = O(n^c log n)
```
Example:
```
T(n) = 2T(n/2) + n

Result:
T(n) = O(n log n)
```

---

### Case 3

If:
```
f(n) = Ω(n^c)
```
where:
```
c > log_b(a)
```
Then:
```
T(n) = O(f(n))
```
Example:
```
T(n) = 2T(n/2) + n²

Result:
T(n) = O(n²)
```
## Applications

- Merge Sort
- Binary Search
- Quick Sort analysis
- Divide-and-conquer algorithms

## Advantages

- Quickly solves many recurrence relations.
- Avoids lengthy expansion of recursive calls.
- Useful for analyzing algorithm efficiency.

## Limitations

- Works only for specific divide-and-conquer recurrences.
- Cannot solve all types of recurrence relations.
- Requires the recurrence to follow the standard form.
