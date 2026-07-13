# Conditional Statements in Java

Conditional statements are used to make decisions in a program. They execute different blocks of code based on whether a condition is `true` or `false`.

## Types of Conditional Statements

### 1. if Statement

Executes a block of code when the condition is true.

### Syntax
```java
if (condition) {
    // code
}
```

### Example
```java
int age = 20;

if (age >= 18) {
    System.out.println("Eligible to vote");
}
```

---

### 2. if-else Statement

Executes one block if the condition is true, otherwise executes another block.

### Syntax
```java
if (condition) {
    // code if true
} else {
    // code if false
}
```

### Example
```java
int marks = 35;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

---

### 3. if-else-if Ladder

Used to check multiple conditions.

```java
if (condition1) {
    // code
} else if (condition2) {
    // code
} else {
    // code
}
```

Example:
```java
int marks = 85;

if (marks >= 90) {
    System.out.println("A+");
} else if (marks >= 75) {
    System.out.println("A");
} else {
    System.out.println("B");
}
```

---

### 4. Nested if

An `if` statement inside another `if` statement.

```java
if (condition1) {
    if (condition2) {
        // code
    }
}
```

---

### 5. switch Statement

Used when comparing a variable with multiple fixed values.

```java
switch(expression) {
    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
```

Example:
```java
int day = 2;

switch(day) {
    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    default:
        System.out.println("Invalid day");
}
```

---

## Key Points

- `if` → Executes code when a condition is true.
- `if-else` → Handles two possible outcomes.
- `if-else-if` → Checks multiple conditions.
- `nested if` → Used for dependent conditions.
- `switch` → Used for multiple fixed choices.
