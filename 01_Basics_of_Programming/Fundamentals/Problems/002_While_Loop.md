# While Loop

## Problem Statement:
A number x is given, we have to print numbers from x to 0 in decreasing order.

## Example:
```
Input: x = 3
Output: 3 2 1 O
```

```
Input: x = 5
Output: 543210
```

Constraints:

O<x<100


---
# Solution:
```java
class Solution {
    public static void utility(int x) {
        // code here
        while(x >= 0){
            System.out.print(x + " ");
            x--;
        }
    }
}
```
