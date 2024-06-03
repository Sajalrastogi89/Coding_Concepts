# Bitwise AND of `x` and `-x` Produces a Mask for the Last Set Bit

## Introduction
When working with binary numbers and bitwise operations, a common task is to isolate the rightmost set bit (i.e., the least significant bit that is set to 1). One efficient way to achieve this is by performing a bitwise AND between a number `x` and its negative `-x`. This operation yields a mask that highlights the position of the last set bit.

## Explanation

### Binary Representation of Positive and Negative Numbers
To understand why this works, let's consider the binary representation of a number and its negative counterpart in two's complement form.

1. **Positive Number (`x`):**
   - Let's take an example, `x = 12`.
   - Binary representation: `00001100`.

2. **Negative Number (`-x`):**
   - The negative of a number in binary is found using two's complement: invert the bits and add 1.
   - Inverting the bits of `00001100` gives `11110011`.
   - Adding 1 to `11110011` results in `11110100`.
   - So, `-12` in binary is `11110100`.

### Bitwise AND Operation
Now, let's perform the bitwise AND operation between `x` and `-x`:

- `x = 00001100`
- `-x = 11110100`

00001100
& 11110100

00000100


The result is `00000100`, which isolates the rightmost set bit of `x`.

### Why This Works
- The rightmost set bit in `x` is the first bit from the right that is `1`.
- In `-x`, all bits after the rightmost set bit (including it) are inverted, and the rest of the bits (to the left) remain the same.
- When `x` and `-x` are ANDed together, all bits except for the rightmost set bit are zeroed out because they are inverted.

### General Case
For any integer `x`, the expression `x & -x` isolates the rightmost set bit. This can be very useful in various algorithms, such as finding the lowest bit set in a number, determining power-of-two properties, or performing bit manipulation tasks efficiently.

## Examples

1. **Example 1:**
   - `x = 10` (binary: `00001010`)
   - `-x = -10` (binary: `11110110`)
   - `x & -x = 00001010 & 11110110 = 00000010`
   - The mask is `00000010`, isolating the second bit.

2. **Example 2:**
   - `x = 20` (binary: `00010100`)
   - `-x = -20` (binary: `11101100`)
   - `x & -x = 00010100 & 11101100 = 00000100`
   - The mask is `00000100`, isolating the third bit.

## Conclusion
Using `x & -x` is a powerful technique in bit manipulation to create a mask for the last set bit. It leverages the properties of two's complement representation and bitwise operations to efficiently isolate the rightmost bit set to `1`.