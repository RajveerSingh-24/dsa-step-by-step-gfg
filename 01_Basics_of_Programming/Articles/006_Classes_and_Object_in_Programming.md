# Classes and Objects in Programming (Java)

## What is a Class?
A **class** is a blueprint or template used to create objects. It defines the properties (variables) and behaviors (methods) that an object will have.

A class does not occupy memory until an object is created.

## What is an Object?
An **object** is an instance of a class. It represents a real-world entity and contains its own data and behavior.

Objects are created using the `new` keyword in Java.

## Syntax

```java
class ClassName {
    // variables
    // methods
}
```
Creating an object:
```java
ClassName objectName = new ClassName();
```

## Example: Class and Object in Java
```java
class Student {

    String name;
    int age;

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {

        // Creating an object
        Student student1 = new Student();

        // Assigning values
        student1.name = "Rajveer";
        student1.age = 20;

        // Calling method
        student1.display();
    }
}
```
Output:
```java
Name: Rajveer
Age: 20
```
---
# Difference Between Class and Object

| Class | Object |
| --- | --- |
| Blueprint for creating objects | Instance of a class |
| Does not occupy memory until object creation | Occupies memory |
| Defines properties and methods | Uses properties and methods |
---
# Advantages of Classes and Objects
- Supports Object-Oriented Programming (OOP)
- Provides code reusability
- Helps organize large programs
- Improves data security through encapsulation
- Makes programs easier to maintain
---
# Key Points
- A class defines the structure of an object.
- An object is created from a class.
- Multiple objects can be created from a single class.
- Objects interact with each other using methods.
- Java is an object-oriented programming language.
