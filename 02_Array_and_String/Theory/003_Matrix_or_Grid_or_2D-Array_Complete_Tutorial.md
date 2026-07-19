# Matrix (Grid / 2D Array) - Complete Tutorial

## What is a Matrix (2D Array)?

A **Matrix** or **2D Array** is a collection of elements arranged in **rows and columns**. It is essentially an array of arrays.

Each element is accessed using two indices:

```text
matrix[row][column]
```

## Characteristics

- Stores elements of the same data type.
- Organized in rows and columns.
- Indexed from `0` in Java.
- Supports constant-time element access.

## Syntax (Java)

```java
// Declaration
int[][] matrix;

// Initialization
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Creating a 3 × 4 matrix
int[][] matrix = new int[3][4];
```

## Accessing Elements

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6}
};

System.out.println(matrix[0][1]); // 2
System.out.println(matrix[1][2]); // 6
```

## Traversing a Matrix

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

for (int i = 0; i < matrix.length; i++) {
    for (int j = 0; j < matrix[i].length; j++) {
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();
}
```

## Updating an Element

```java
matrix[1][1] = 10;
```

## Advantages

- Represents tabular data efficiently.
- Fast element access using indices.
- Useful for mathematical computations and grid-based problems.

## Disadvantages

- Fixed size after creation.
- Insertion and deletion are expensive.
- Requires contiguous memory.

## Time Complexity

| Operation | Complexity |
|-----------|------------|
| Access | O(1) |
| Update | O(1) |
| Traverse | O(R × C) |
| Search | O(R × C) |

Where:
- `R` = Number of rows
- `C` = Number of columns

## Applications

- Matrix operations
- Image processing
- Game boards (Chess, Sudoku, Tic-Tac-Toe)
- Dynamic Programming
- Graph representation
- Grid-based algorithms (BFS, DFS)
