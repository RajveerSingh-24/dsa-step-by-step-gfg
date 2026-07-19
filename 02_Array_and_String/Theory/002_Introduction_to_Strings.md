# Introduction to Strings

## What is a String?

A **String** is a sequence of characters used to represent text. In Java, strings are objects of the `String` class and are **immutable**, meaning their value cannot be changed after creation.

## Characteristics

- Stores a sequence of characters.
- Indexed starting from `0`.
- Immutable in Java.
- Provides many built-in methods for manipulation.

## Syntax (Java)

```java
// String Declaration
String str;

// String Initialization
String str = "Hello, World!";

// Creating a String using constructor
String str = new String("Hello");
```

## Accessing Characters

```java
String str = "Java";

System.out.println(str.charAt(0)); // J
System.out.println(str.charAt(2)); // v
```

## Common String Methods

```java
String str = "Hello";

System.out.println(str.length());          // 5
System.out.println(str.toUpperCase());     // HELLO
System.out.println(str.toLowerCase());     // hello
System.out.println(str.substring(1, 4));   // ell
System.out.println(str.contains("ell"));   // true
```

## String Concatenation

```java
String first = "Hello";
String second = "World";

String result = first + " " + second;

System.out.println(result); // Hello World
```

## Advantages

- Easy to store and manipulate text.
- Rich set of built-in methods.
- Immutable, making strings safe to use.

## Disadvantages

- Immutable, so modifications create new objects.
- Frequent modifications can be less memory-efficient.

## Time Complexity

| Operation | Complexity |
|-----------|------------|
| Access Character | O(1) |
| Length | O(1) |
| Concatenation (`+`) | O(N) |
| Substring | O(N) |
| Comparison | O(N) |

## Applications

- Text processing.
- User input handling.
- File and data parsing.
- Searching and pattern matching.
- Web development and APIs.
