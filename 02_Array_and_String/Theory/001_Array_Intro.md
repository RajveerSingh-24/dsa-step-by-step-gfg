# Introduction to Arrays

## What is an Array?

An **array** is a linear data structure that stores a fixed number of elements of the **same data type** in contiguous memory locations.

Each element is identified by its **index**, which starts from `0` in Java.

## Characteristics

- Stores elements of the same data type.
- Elements are stored in contiguous memory.
- Supports fast access using indices.
- Has a fixed size after creation.

## Syntax (Java)

```java
// Declaration
int[] arr;

// Declaration and Initialization
int[] arr = {10, 20, 30, 40, 50};

// Creating an array of size 5
int[] arr = new int[5];
```

## Accessing Elements

```java
int[] arr = {10, 20, 30};

System.out.println(arr[0]); // 10
System.out.println(arr[2]); // 30
```

## Updating Elements

```java
int[] arr = {10, 20, 30};

arr[1] = 50;

System.out.println(arr[1]); // 50
```

## Advantages

- Fast element access using index (`O(1)`).
- Simple to implement and use.
- Efficient memory usage due to contiguous storage.

## Disadvantages

- Fixed size.
- Insertion and deletion are costly.
- Can store only one data type.

## Time Complexity

| Operation | Complexity |
|-----------|------------|
| Access | O(1) |
| Search | O(N) |
| Update | O(1) |
| Insertion (middle) | O(N) |
| Deletion (middle) | O(N) |

## Applications

- Storing collections of data.
- Matrix representation.
- Implementing stacks, queues, and hash tables.
- Basis for many other data structures.
