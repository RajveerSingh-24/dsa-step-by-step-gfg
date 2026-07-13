# While Loop in Java

A **while loop** is used to repeatedly execute a block of code as long as a given condition is **true**. It is generally used when the number of iterations is not known beforehand.

## Syntax

```java
while(condition) {
    // code to execute
}
```
- Condition → Checked before every iteration.
- The loop stops when the condition becomes false.

## Example
```java
public class Main {
    public static void main(String[] args) {

        int i = 1;

        while(i <= 5) {
            System.out.println(i);
            i++;
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
# Key Points
- Condition is checked before execution.
- Useful when the number of iterations is unknown.
- The loop variable must be updated inside the loop to avoid infinite loops.
- break is used to exit the loop.
- continue is used to skip the current iteration.
