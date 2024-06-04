# BigInteger in Java

## Introduction
The `BigInteger` class in Java is part of the `java.math` package and is used to represent arbitrarily large integers. It provides operations for arithmetic, comparison, and bitwise manipulation on integers of any size.

## Features
- **Arbitrary Precision:** BigInteger can represent integers of any size, limited only by available memory.
- **Immutable:** BigInteger objects are immutable, meaning their values cannot be changed after creation.
- **Supports Operations:** BigInteger supports all basic arithmetic operations such as addition, subtraction, multiplication, and division, as well as comparison and bit manipulation operations.
- **Exception Handling:** BigInteger methods throw `ArithmeticException` when arithmetic operations result in overflow or division by zero.

## Usage
```java
import java.math.BigInteger;

public class Main {
    public static void main(String[] args) {
        BigInteger bigInt1 = new BigInteger("123456789012345678901234567890");
        BigInteger bigInt2 = BigInteger.valueOf(987654321098765432109876543210);
        
        // Addition
        BigInteger sum = bigInt1.add(bigInt2);
        System.out.println("Sum: " + sum);
        
        // Multiplication
        BigInteger product = bigInt1.multiply(bigInt2);
        System.out.println("Product: " + product);
        
        // Comparison
        int comparison = bigInt1.compareTo(bigInt2);
        System.out.println("Comparison: " + comparison);
    }
}
