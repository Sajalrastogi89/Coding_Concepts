# Integer Class in Java

## Introduction
The `Integer` class in Java is a wrapper class for the primitive type `int`. It provides utility methods for converting between `int` values and `String`, as well as performing arithmetic operations, comparison, and bit manipulation on integer values.

## Features
- **Wrapper Class:** Integer serves as a wrapper class for the `int` primitive data type in Java, allowing it to be treated as an object.
- **Conversion:** Integer class provides methods to convert integer values to and from strings (`toString`, `parseInt`). Additionally, it supports methods for converting binary strings to integers and integers to binary strings.
- **Arithmetic Operations:** Integer supports basic arithmetic operations such as addition, subtraction, multiplication, and division.
- **Comparison:** Integer objects can be compared using methods like `compareTo`.
- **Bit Manipulation:** Integer class supports bitwise operations like AND, OR, and XOR.
- **Immutable:** Integer objects are immutable, meaning their values cannot be changed after instantiation.

## Usage
```java
Integer num1 = Integer.valueOf(10);
Integer num2 = Integer.parseInt("20");

// Arithmetic Operations
int sum = Integer.sum(num1, num2);
int product = Integer.multiply(num1, num2);

// Comparison
int result = num1.compareTo(num2);

// Bit Manipulation
int bitwiseAnd = num1 & num2;
int bitwiseOr = num1 | num2;

// Binary to Integer Conversion
int binaryToInt = Integer.parseInt("1010", 2);

// Integer to Binary String Conversion
String intToBinary = Integer.toBinaryString(10);
