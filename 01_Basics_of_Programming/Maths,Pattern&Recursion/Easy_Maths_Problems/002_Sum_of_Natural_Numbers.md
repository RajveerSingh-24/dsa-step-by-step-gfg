# Sum of Natural Numbers

## Problem

Find the sum of the first `N` natural numbers.

## Approach

The sum of natural numbers from `1` to `N` can be calculated using the formula:
```java
Sum = N * (N + 1) / 2
```

This avoids using loops and gives the result in constant time.

## Code (Java - Optimal)

```java
class Solution {
    public static long sumOfNaturals(long n) {
        return n * (n + 1) / 2;
    }
}
```

## Another Solution using Loops:
```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        // code here
        int sum = 0;
        for(int i = 1;i <= n;i++){
            sum+=i;
        }
        System.out.print(sum);
    }
}
```
