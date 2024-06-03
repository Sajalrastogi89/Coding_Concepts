# Using Modulus with Addition, Subtraction, and Multiplication (but not Division)

## Introduction
The modulus operation is an important concept in number theory and computer science, particularly in arithmetic and algorithm design. This note explains why the modulus operation can be applied in conjunction with addition, subtraction, and multiplication but not with division.

## Explanation

### Modulus Operation
The modulus operation finds the remainder of the division of one number by another. Given two integers \( a \) and \( b \), the expression \( a \% b \) yields the remainder when \( a \) is divided by \( b \).

### Modulus with Addition
If \( a \% m \) and \( b \% m \) are known, then:
\[ (a + b) \% m = [(a \% m) + (b \% m)] \% m \]

This property allows you to perform addition modulo \( m \) by taking the sum of the individual remainders and then taking the remainder of the result.

### Modulus with Subtraction
If \( a \% m \) and \( b \% m \) are known, then:
\[ (a - b) \% m = [(a \% m) - (b \% m) + m] \% m \]

The extra addition of \( m \) ensures the result is non-negative.

### Modulus with Multiplication
If \( a \% m \) and \( b \% m \) are known, then:
\[ (a \cdot b) \% m = [(a \% m) \cdot (b \% m)] \% m \]

This property allows you to perform multiplication modulo \( m \) by taking the product of the individual remainders and then taking the remainder of the result.

### Why Not Division?
The modulus operation does not apply directly with division. The problem arises because division is not a closed operation in modular arithmetic. In simpler terms, dividing two numbers modulo \( m \) does not always yield a unique result that is within the same modular system.

#### Example:
Consider \( a \% m \) and \( b \% m \):
\[ (a / b) \% m \]

Unlike addition, subtraction, and multiplication, there is no straightforward method to compute this because division in modular arithmetic requires the concept of modular inverses.

#### Modular Inverse
To divide \( a \) by \( b \) under modulo \( m \), you need to multiply \( a \) by the modular inverse of \( b \) modulo \( m \), denoted as \( b^{-1} \). The modular inverse exists only if \( b \) and \( m \) are coprime (i.e., \( \text{gcd}(b, m) = 1 \)).

\[ (a / b) \% m = (a \cdot b^{-1}) \% m \]

Finding the modular inverse is not always feasible, making direct division under modulus complicated and often impractical.

## Conclusion
While the modulus operation can be seamlessly integrated with addition, subtraction, and multiplication due to the closure properties of these operations within modular arithmetic, division requires a modular inverse and is not inherently supported. This limitation arises from the fundamental differences in how division operates compared to the other arithmetic operations.

