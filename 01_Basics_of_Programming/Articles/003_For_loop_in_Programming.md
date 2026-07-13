# For Loop in Java

A **for loop** is used to execute a block of code repeatedly for a fixed number of times. It is commonly used when the number of iterations is known.

## Syntax

```java
for(initialization; condition; update) {
    // code to execute
}
```
- Initialization → Executes once at the beginning.
- Condition → Loop runs while this condition is true.
- Update → Changes the loop variable after every iteration.

## Example

```java
public class Main {
    public static void main(String[] args) {
        for(int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

## Output

```
1
2
3
4
5
```
---
# Nested For Loop

A loop inside another loop is called a nested loop.

```java
for(int i = 1; i <= 3; i++) {
    for(int j = 1; j <= 3; j++) {
        System.out.println(i + " " + j);
    }
}
```


## Output

```
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

---
# Enhanced For Loop (For-each)
Used to iterate through arrays or collections.

## Syntax
```java
for(dataType variable : array) {
    // code
}
```

## Example
```java
int[] arr = {10, 20, 30};

for(int num : arr) {
    System.out.println(num);
}
```
## Output
```
10
20
30
```
---
# Key Points
- Used when the number of iterations is known.
- Helps reduce repetitive code.
- Can be used with arrays and collections.
- break is used to exit a loop.
- continue skips the current iteration.
