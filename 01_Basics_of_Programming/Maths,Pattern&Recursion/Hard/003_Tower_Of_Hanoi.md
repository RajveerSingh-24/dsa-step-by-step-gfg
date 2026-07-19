# Tower of Hanoi

## Problem

Given `N` disks and three rods (**Source**, **Auxiliary**, and **Destination**), move all the disks from the source rod to the destination rod following these rules:

- Only one disk can be moved at a time.
- A larger disk cannot be placed on top of a smaller disk.
- Only the top disk of a rod can be moved.

## Approach

- Use **recursion**.
- Move the top `N - 1` disks from the source to the auxiliary rod.
- Move the largest disk to the destination rod.
- Move the `N - 1` disks from the auxiliary to the destination rod.

## Code (Java)

```java
class Solution {

    static void towerOfHanoi(int n, char source, char auxiliary, char destination) {
        if (n == 1) {
            System.out.println("Move disk 1 from " + source + " to " + destination);
            return;
        }

        towerOfHanoi(n - 1, source, destination, auxiliary);

        System.out.println("Move disk " + n + " from " + source + " to " + destination);

        towerOfHanoi(n - 1, auxiliary, source, destination);
    }

    public static void main(String[] args) {
        int n = 3;
        towerOfHanoi(n, 'A', 'B', 'C');
    }
}
```

## Example

Input:

```text
N = 3
```

Output:

```text
Move disk 1 from A to C
Move disk 2 from A to B
Move disk 1 from C to B
Move disk 3 from A to C
Move disk 1 from B to A
Move disk 2 from B to C
Move disk 1 from A to C
```

## Complexity Analysis

- **Time Complexity:** O(2ᴺ)
- **Space Complexity:** O(N) (Recursion Stack)

## Concept Used

- Recursion
- Divide and Conquer
- Backtracking
