# Input Output in C

```c
#include <stdio.h>

int main() {
    int age;
    float height;
    char grade;
    char name[20];

    // Asking for input
    printf("Enter your age, height, grade, and name: ");

    // Reading input from the user
    scanf("%d %f %c %s", &age, &height, &grade, name);

    // Displaying the input using printf
    printf("Your age: %d\n", age);
    printf("Your height: %.2f\n", height);  // .2f for 2 decimal places
    printf("Your grade: %c\n", grade);
    printf("Your name: %s\n", name);

    return 0;
}
```
---

# Input Output in CPP
```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    float height;
    char grade;
    string name;

    cout << "Enter your age, height, grade, and name: ";
    cin >> age >> height >> grade >> name;

    cout << "Your age: " << age << "\n";
    cout << "Your height: " << height << "\n";
    cout << "Your grade: " << grade << "\n";
    cout << "Your name: " << name << "\n";

    return 0;
}
```
---

# Input Output in Java
```java
import java.util.Scanner;

public class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age, height, grade, and name: ");
        int age = sc.nextInt();
        float height = sc.nextFloat();
        char grade = sc.next().charAt(0);
        String name = sc.next();

        System.out.println("Your age: " + age);
        System.out.println("Your height: " + height);
        System.out.println("Your grade: " + grade);
        System.out.println("Your name: " + name);
    }
}
```
---
# Input Output in Python
```python
age, height, grade, name = input("Enter your age, height, grade, and name: ").split()

age = int(age)
height = float(height)
grade = grade
name = name

print("Your age:", age)
print("Your height:", height)
print("Your grade:", grade)
print("Your name:", name)
```

---
Input:
```
20 5.9 A Alice
```

---
Output:
```
Your age: 20
Your height: 5.9
Your grade: A
Your name: Alice
```


