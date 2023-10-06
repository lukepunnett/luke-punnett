---
layout: post
title: Total Java Guide
description: Ipsum dolor sit amet
image: assets/images/pic04.jpg
---

1. What & Why Java?
2. Getting Started
3. Data Types & Variables
4. Operators
5. Control Structures- Conditionals & Loops
6. Functions
7. Data Structures
8. Classes and Objects
9. Inheritance
10. Polymorphism
11. Interfaces
12. Exception Handling
13. Input & Output
14. Next Steps

## What & Why Java
   - Platform independence: Java is designed to be platform-independent, meaning that once a program is written, it can be run on any platform that has a Java Virtual Machine (JVM) installed.
   - Robustness: Java is designed to be a robust and reliable programming language, with features such as memory management and exception handling built in.
   - Object-oriented programming: Java is an object-oriented programming language, which means that it provides a natural and flexible way to model real-world objects and their relationships.
   - Large community: Java has a large and active community of developers, which means that there are many resources available for learning, support, and collaboration.
   - Performance: While Java may not be the fastest language out there, it is highly optimized for performance and can handle complex tasks efficiently.
   - Security: Java provides a secure runtime environment with features such as automatic memory management, byte-code verification, and sandboxing.
   - Versatility: Java can be used for a wide range of applications, from desktop and mobile applications to web and enterprise applications.
   - Scalability: Java's architecture is designed to be scalable, meaning that it can handle large and complex applications with ease.
   - Popular frameworks: Java has many popular and powerful frameworks, such as Spring, Hibernate, and Struts, which can make development faster and easier.
   - Support for multiple paradigms: Java supports multiple programming paradigms, including procedural, object-oriented, and functional programming, making it flexible and adaptable to different programming styles.

## Getting Started

## Data Types and Variables
1. Overview 
2. Primitive Data Types
3. Reference Data Types
4. Java Variable Syntax
5. Constants
6. Variable Scope
7. Best Practices

A variable is a named container that stores a value of a particular data type. In Java, variables are used to hold values that can be manipulated and used throughout a program.

Variables can be of two types in Java: primitive types and reference types.

### Primitive Variables

Primitive variables are used to store simple values like numbers and characters. The following are the primitive data types available in Java:

- byte: 8-bit integer value
- short: 16-bit integer value
- int: 32-bit integer value
- long: 64-bit integer value
- float: 32-bit floating-point value
- double: 64-bit floating-point value
- char: 16-bit Unicode character value
- boolean: true or false value

Primitive variables are declared using a data type keyword, followed by the variable name, and optionally, an initial value. For example, to declare an integer variable named "count" with an initial value of 0, you would write:
```java
int count = 0;
```

### Reference Variables

Reference variables are used to store object references, which point to objects in memory. Reference variables are declared using the class name of the object they reference, followed by the variable name, and optionally, an initial value. For example, to declare a reference variable named "myObject" that refers to an instance of the String class, you would write:
```java
String myObject = new String("Hello, World!");
```
In this example, the new keyword creates a new instance of the String class, and the reference variable myObject points to this new object.

### Differences between Reference and Primitive data in Java

In Java, primitive types and reference types (also known as objects) are handled differently in memory. Here are the main differences:

- Memory allocation: Primitive types are stored on the stack, whereas reference types are stored on the heap. When a primitive type is declared, memory is allocated on the stack at the point where the variable is defined. When a reference type is declared, a memory address (i.e. a reference) is allocated on the stack, but the object itself is allocated on the heap.

- Size: Primitive types have a fixed size that is determined by the type, whereas reference types have a variable size that depends on the object being stored.

- Default values: Primitive types have default values (e.g. 0 for int, false for boolean) if they are not initialized explicitly, whereas reference types have a default value of null if they are not initialized explicitly.

- Passing by value vs. passing by reference: When a primitive type is passed as an argument to a method, a copy of its value is passed (i.e. passed by value), whereas when a reference type is passed as an argument to a method, a copy of the reference (i.e. the memory address) is passed (i.e. passed by reference). This means that when the method modifies the object, the changes are reflected outside the method.

- Garbage collection: Objects on the heap are subject to garbage collection, whereas primitive types are not. When an object is no longer referenced by any variables or objects, it becomes eligible for garbage collection, and the memory it occupied is released by the JVM.

These differences between primitive and reference types can affect the performance and behavior of your Java program, so it's important to understand them and use them appropriately.

#### Heap vs Stack Memory in Java
In Java, the heap and the stack are two distinct regions of memory that are used to store different types of data.

The heap is a region of memory that is used to store objects and arrays. When you create an object in Java, memory is allocated on the heap to store the object's data. Similarly, when you create an array, memory is allocated on the heap to store the array's elements. The size of the heap is determined by the JVM's configuration and is not fixed, meaning that it can grow or shrink dynamically as needed. The heap is managed by the JVM's garbage collector, which is responsible for freeing up memory that is no longer being used by your program.

The stack, on the other hand, is a region of memory that is used to store method invocations and local variables. When a method is called, a new frame is added to the top of the stack to store information about the method's arguments and local variables. When the method returns, the frame is removed from the stack. The stack is a fixed size and is determined by the JVM's configuration, meaning that it cannot grow or shrink dynamically.

Because the heap is used to store objects and arrays, which can be large and complex, it tends to be slower than the stack. On the other hand, the stack is used to store smaller and simpler data, such as primitive variables and method invocations, so it tends to be faster than the heap. This is because the stack is organized in a Last-In-First-Out (LIFO) structure, which makes it faster and easier for the CPU to access and manipulate data.

In summary, the heap and the stack are two distinct regions of memory in Java that are used to store different types of data. The heap is used to store objects and arrays, while the stack is used to store method invocations and local variables. Understanding the differences between these two regions of memory is important for optimizing the performance and memory usage of your Java programs.
    
### Variable Naming Conventions
It's important to follow naming conventions when naming variables in Java. Variable names should be descriptive, concise, and follow a standard naming convention. In Java, the standard convention for naming variables is to use camelCase, where the first word is in lowercase and the first letter of each subsequent word is capitalized. For example:
```java
int studentCount;
String customerName;
```
By following these conventions, your code will be more readable and easier to understand for other developers who may need to work with your code.

### Java Variable Syntax

In Java, variable names follow similar rules to those in other programming languages, but there are some specific guidelines to keep in mind. Here are some common rules for naming variables in Java:

 - Variable names must begin with a letter, underscore (_), or dollar sign ($).
 - Variable names can contain letters, digits, underscores, and dollar signs.
 - Variable names are case-sensitive.
 - Variable names should be written in camelCase convention, starting with a lowercase letter, and using a capital letter for each new word within the variable name.
 - Avoid using reserved words or keywords that have a special meaning in Java. For example, you cannot use "class" or "public" as a variable name since they are reserved words.
 - Use meaningful and descriptive variable names to make your code more readable and maintainable.
 - Avoid using abbreviations or acronyms that may not be clear to others who read your code.
 - Variables that are constants should be written in uppercase letters, using underscores to separate words.

For example, a variable representing a person's age could be named "personAge" or "ageOfPerson" in Java, using camelCase convention. A constant value for the speed of light could be named "SPEED_OF_LIGHT" using uppercase letters and underscores to separate words.

### Reserved or Keywords in Java

Java keywords are reserved words in the Java programming language that have a specific meaning and cannot be used as identifiers, such as variable names, class names, or method names. These keywords are used to define the structure and behavior of Java programs, and they have a special meaning in the Java language.

It is important to note that these keywords cannot be used as identifiers or variable names in Java, as doing so will result in a syntax error.

### Variable Scope
The scope of a variable determines where it can be accessed in a program. In Java, variables can have different scopes depending on where they are declared. The following are the different types of variable scopes in Java:

- Local scope: Variables declared inside a method or block of code have local scope and can only be accessed within that method or block.
- Instance scope: Variables declared inside a class but outside of any method have instance scope and can be accessed by any method of the class.
- Class scope: Variables declared as static inside a class have class scope and can be accessed by any method of the class.


### Constants

In Java, a constant is a variable whose value cannot be changed once it has been initialized. Constants are typically used to represent fixed values in a program, such as mathematical constants or configuration values that are unlikely to change during runtime.

To declare a constant in Java, you use the "final" keyword followed by the data type, variable name, and initial value. For example:

```java
final double PI = 3.14159;
final int MAX_VALUE = 100;
final String APPLICATION_NAME = "My Java App";
```
Once a constant has been declared, its value cannot be changed. Attempting to assign a new value to a constant will result in a compilation error.

Constants are often used in Java programs to provide meaningful names for values that are used repeatedly in the code. For example, a program that calculates the area of a circle might use the constant "PI" to represent the mathematical constant pi, rather than hard-coding the value in the program. This can make the code more readable and easier to maintain.

It is common practice to name constants using all uppercase letters with underscores to separate words. This makes them easily distinguishable from other variables in the code, and indicates that their values should not be changed during program execution.

#### Class Level Constants

In Java, class-level constants are typically defined using the static final keywords. These constants are variables that are associated with the class itself rather than with any particular instance of the class, and their values cannot be changed once they are initialized.

Here's an example of defining a class-level constant in Java:
```java
public class MyClass {
  public static final int MY_CONSTANT = 42;
}
```
In this example, MY_CONSTANT is a class-level constant that is of type int and has a value of 42. Because it is declared with the static keyword, this constant is associated with the class itself rather than with any particular instance of the class. Because it is declared with the final keyword, its value cannot be changed once it is initialized.

So why would you want to use class-level constants in Java? Here are a few reasons:

- Constants help to make your code more readable and maintainable. By using constants instead of hardcoding values throughout your code, it's easier to understand the purpose of the values and to make changes if needed.

- Constants can be used to improve performance. By using constants instead of variables, the Java compiler can optimize your code more effectively and reduce the amount of memory that your program uses.

- Constants can be used to ensure consistency across your codebase. By defining constants at the class level, you can ensure that all instances of the class use the same values for those constants, which can help to prevent bugs and make your code more reliable.

### Best Practices for Variables

Here are some best practices to consider when it comes to variables in Java:

- Use meaningful variable names: Choose variable names that clearly convey the purpose of the variable. Avoid using single-letter variable names or abbreviations that might be unclear to others who read your code.

- Limit the scope of variables: Declare variables in the smallest scope possible. This helps to prevent unintentional changes to the variable's value and makes it easier to reason about the behavior of your code.

- Initialize variables when you declare them: Always initialize your variables when you declare them, even if the initial value is null or zero. This helps to prevent NullPointerExceptions and other bugs.

- Use final whenever possible: Declare your variables as final whenever possible. This helps to prevent accidental changes to the variable's value and can improve the performance of your code.

- Use primitive types when appropriate: Use primitive types (e.g. int, boolean, double) when appropriate, as they are more efficient than objects and take up less memory.

- Avoid using magic numbers: Avoid using "magic numbers" (i.e. hard-coded values) in your code. Instead, use named constants or variables to make your code more readable and maintainable.

- Be careful with null values: Be careful when using null values, as they can cause NullPointerExceptions if not handled properly. Consider using Optional or other techniques to handle null values in a more robust way.

- Use data types that are appropriate for the data you are storing: Choose data types that are appropriate for the data you are storing. For example, use String for text data, and use collections (e.g. List, Map) for storing multiple values.

By following these best practices, you can write more readable, maintainable, and reliable code in Java.

## Operators
Java has several types of operators that can be used to perform different types of operations on variables and values. Here's an overview of the most common operators in Java:

### Arithmetic operators
These operators are used to perform basic mathematical operations on numeric values. The arithmetic operators in Java are:

    + (addition)
    - (subtraction)
    * (multiplication)
    / (division)
    % (modulus, returns the remainder of a division operation)

### Assignment operators
These operators are used to assign a value to a variable. The assignment operators in Java are:

    = (simple assignment)
    += (addition assignment)
    -= (subtraction assignment)
    *= (multiplication assignment)
    /= (division assignment)
    %= (modulus assignment)

### Comparison operators
These operators are used to compare two values and return a Boolean value (true or false) depending on the result of the comparison. The comparison operators in Java are:

    == (equal to)
    != (not equal to)
    > (greater than)
    < (less than)
    >= (greater than or equal to)
    <= (less than or equal to)

### Logical operators
These operators are used to combine Boolean values and return a Boolean result. The logical operators in Java are:

    && (logical AND, returns true if both operands are true)
    || (logical OR, returns true if either operand is true)
    ! (logical NOT, returns the opposite of the operand's value)

### Bitwise operators
These operators are used to perform bitwise operations on integer values. The bitwise operators in Java are:

    & (bitwise AND)
    | (bitwise OR)
    ^ (bitwise XOR, returns 1 if the bits are different, 0 if they are the same)
    ~ (bitwise NOT, returns the complement of the operand)
    << (left shift, shifts the bits to the left)
    >> (signed right shift, shifts the bits to the right and preserves the sign bit)
    >>> (unsigned right shift, shifts the bits to the right and fills the leftmost bits with zeroes)

These are the most common operators in Java, but there are other operators as well, such as the conditional operator (?:) and the instanceof operator. It's important to understand how these operators work and how to use them effectively in your Java programs.

Bitwise operations in Java are operations that manipulate individual bits of binary numbers. These operations work on the individual bits of integers or other binary data at the bit level. There are several bitwise operators in Java:

1. **AND (&)**: The bitwise AND operator compares each bit of the first operand to the corresponding bit of the second operand. If both bits are 1, the resulting bit is 1. Otherwise, it's 0.

2. **OR (|)**: The bitwise OR operator compares each bit of the first operand to the corresponding bit of the second operand. If either of the bits is 1, the resulting bit is 1. If both bits are 0, the resulting bit is 0.

3. **XOR (^)**: The bitwise XOR (exclusive OR) operator compares each bit of the first operand to the corresponding bit of the second operand. If the bits are different (one is 0 and the other is 1), the resulting bit is 1. If the bits are the same (both 0 or both 1), the resulting bit is 0.

4. **NOT (~)**: The bitwise NOT operator flips each bit. If a bit is 0, it becomes 1, and if a bit is 1, it becomes 0.

5. **Left Shift (<<)**: The left shift operator shifts all the bits in a binary number to the left by a specified number of positions. This is equivalent to multiplying the number by 2 raised to the power of the shift count.

6. **Right Shift (>>)**: The right shift operator shifts all the bits in a binary number to the right by a specified number of positions. This is equivalent to dividing the number by 2 raised to the power of the shift count.

7. **Unsigned Right Shift (>>>)**: The unsigned right shift operator shifts all the bits to the right, filling the leftmost bits with zeros.

Bitwise operations are used for various purposes, including:

- **Optimizing Performance**: Bitwise operations are often faster than arithmetic operations, making them useful for optimizing performance in certain situations.

- **Manipulating Individual Bits**: Bitwise operations are used to manipulate and set individual bits within integers, particularly in fields like cryptography, graphics, networking, and low-level system programming.

- **Flag Manipulation**: They are commonly used to represent and manipulate flags or options within a single integer, where each bit corresponds to a specific flag.

- **Data Compression and Encoding**: Bitwise operations are used in various data compression and encoding algorithms to manipulate bits and optimize data storage.

- **Masking**: Bitwise operations are used to mask specific bits in a value, allowing you to isolate or extract certain information from a bit pattern.

Overall, bitwise operations are powerful tools for working with binary data and optimizing certain algorithms and operations.

### Control Structures

1. Conditionals
2. For Loops
3. While Loops
4. Do-while Loops
5. Switch Statements

In Java, control structures are used to control the flow of execution in a program. They allow you to make decisions based on conditions, repeat code blocks, and jump to different parts of the program based on certain conditions. Here's an overview of the most common control structures in Java

#### Conditionals (if statements) 

Conditionals are a type of control structure in programming that allow you to execute different code blocks based on certain conditions. In Java, the most common conditional statement is the if-else statement, which has the following syntax:
```
if (condition) {
  // code to execute if the condition is true
} else {
  // code to execute if the condition is false
}
```

The condition in the if statement is typically a Boolean expression that evaluates to true or false. If the condition is true, the code block inside the if statement is executed. If the condition is false, the code block inside the else statement is executed (if there is one).

In addition to the if-else statement, Java also supports a shorthand version of the if statement called the **ternary** operator. It has the following syntax:
```
variable = (condition) ? value1 : value2;
```

This is useful when you want to assign a value to a variable based on a condition. If the condition is true, the variable is assigned the value of value1. If the condition is false, the variable is assigned the value of value2.

Java also supports nested if-else statements, which allow you to test multiple conditions in a row. Here's an example of a nested if-else statement:
```
if (condition1) {
  // code to execute if condition1 is true
  if (condition2) {
    // code to execute if both condition1 and condition2 are true
  } else {
    // code to execute if condition1 is true but condition2 is false
  }
} else {
  // code to execute if condition1 is false
}
```

In addition to if-else statements, Java also supports switch statements, which allow you to execute different code blocks based on the value of a variable or expression. Here's an example of a switch statement:
```
switch (expression) {
  case value1:
    // code to execute if expression equals value1
    break;
  case value2:
    // code to execute if expression equals value2
    break;
  default:
    // code to execute if expression does not match any of the cases above
    break;
}
```

In summary, conditionals are an important type of control structure in Java that allow you to execute different code blocks based on certain conditions. By understanding how to use if-else statements, ternary operators, nested if-else statements, and switch statements, you can write more efficient and readable code.

### Java Methods
#### Java Method Basics

Methods are blocks of code that perform a specific task, and they are executed when they are called upon by other parts of a program.

Here are the main components of a Java method:

    Method Signature: This includes the access modifier (public, private, protected), the return type (void, int, String, etc.), the method name, and the parameter list (if any).

    Method Body: This is where the actual code that performs the task is written.

Here's an example of a basic method:
```
public void printMessage(String message) {
  System.out.println(message);
}
```
In this method, the access modifier is "public", the return type is "void" (meaning the method doesn't return anything), the method name is "printMessage", and the parameter is a String called "message". The method body simply prints out the message passed to it using the System.out.println method.

To call this method, you would simply write:
```
printMessage("Hello, world!");
```
And the output would be:
```
Hello, world!
```
Java also supports methods with a return value. Here's an example:
```
public int addNumbers(int a, int b) {
  return a + b;
}
```
In this method, the return type is "int" (meaning the method returns an integer), the method name is "addNumbers", and the parameters are two integers called "a" and "b". The method body simply adds the two integers together and returns the result.

To call this method, you would write:
```
int result = addNumbers(5, 7);
System.out.println(result);
```
And the output would be:
```
12
```
#### Access Modifiers

In Java, access modifiers determine the level of access that a class, method, or variable has to other parts of the program. There are four access modifiers in Java:

    Public
    Protected
    Default (also known as package-private)
    Private

Let's take a closer look at each one:

    Public: A public class, method, or variable can be accessed from anywhere in the program. This means that any part of the program can create an instance of a public class, call a public method, or access a public variable. Here's an example:
    ```
    public class MyClass {
  public int myPublicVariable = 10;

  public void myPublicMethod() {
    // Code goes here
  }
}
```
In this example, the MyClass class is declared as public, which means it can be accessed from anywhere in the program. The myPublicVariable variable and myPublicMethod() method are also declared as public, which means they can be accessed from anywhere in the program as well.

    Protected: A protected class, method, or variable can be accessed from within the same package (group of classes in the same directory) or from a subclass (a class that inherits from another class). This means that any class in the same package as a protected class, or any subclass of a protected class, can access its protected members. Here's an example:
    ```
    public class MyClass {
  protected int myProtectedVariable = 10;

  protected void myProtectedMethod() {
    // Code goes here
  }
}
    ```
    Sure, I'd be happy to teach you about Java access modifiers!

In Java, access modifiers determine the level of access that a class, method, or variable has to other parts of the program. There are four access modifiers in Java:

    Public
    Protected
    Default (also known as package-private)
    Private

Let's take a closer look at each one:

    Public: A public class, method, or variable can be accessed from anywhere in the program. This means that any part of the program can create an instance of a public class, call a public method, or access a public variable. Here's an example:

csharp

public class MyClass {
  public int myPublicVariable = 10;

  public void myPublicMethod() {
    // Code goes here
  }
}

In this example, the MyClass class is declared as public, which means it can be accessed from anywhere in the program. The myPublicVariable variable and myPublicMethod() method are also declared as public, which means they can be accessed from anywhere in the program as well.

    Protected: A protected class, method, or variable can be accessed from within the same package (group of classes in the same directory) or from a subclass (a class that inherits from another class). This means that any class in the same package as a protected class, or any subclass of a protected class, can access its protected members. Here's an example:

csharp

public class MyClass {
  protected int myProtectedVariable = 10;

  protected void myProtectedMethod() {
    // Code goes here
  }
}

In this example, the myProtectedVariable variable and myProtectedMethod() method are declared as protected. This means that any class in the same package as MyClass, or any subclass of MyClass, can access its protected members.

    Default: A default (or package-private) class, method, or variable can be accessed only from within the same package. This means that any class in the same package as a default member can access it, but classes in other packages cannot. Here's an example:
    ```
    class MyClass {
  int myDefaultVariable = 10;

  void myDefaultMethod() {
    // Code goes here
  }
}
```
In this example, the MyClass class, myDefaultVariable variable, and myDefaultMethod() method are all declared without an access modifier, which means they are default members. This means that they can only be accessed from within the same package.

    Private: A private class, method, or variable can be accessed only from within the same class. This means that no other class, even one in the same package or subclass, can access its private members. Here's an example:

    ```
    public class MyClass {
  private int myPrivateVariable = 10;

  private void myPrivateMethod() {
    // Code goes here
  }
}
    ```
In this example, the myPrivateVariable variable and myPrivateMethod() method are declared as private. This means that they can only be accessed from within the MyClass class.

These are the four access modifiers in Java. By using these access modifiers, you can control the level of access that classes, methods, and variables have to other parts of your program.
