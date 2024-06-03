# Using `n & (n - 1)` to Remove the Rightmost Set Bit

## Introduction
In binary operations, an interesting and useful technique is to use the expression `n & (n - 1)` to remove the rightmost set bit from a number. This operation is widely used in various algorithms, such as counting the number of set bits (Hamming weight) in a number.

## Explanation

### Binary Representation of `n` and `n - 1`
To understand why `n & (n - 1)` works, we need to examine the binary representations of `n` and `n - 1`.

1. **Number `n`:**
   - Let's take an example, `n = 12`.
   - Binary representation: `00001100`.

2. **Number `n - 1`:**
   - Subtracting 1 from `n` flips all the bits after the rightmost set bit (including the rightmost set bit itself).
   - For `n = 12`, `n - 1 = 11`.
   - Binary representation of `11`: `00001011`.

### Bitwise AND Operation
Now, let's perform the bitwise AND operation between `n` and `n - 1`:

- `n = 00001100`
- `n - 1 = 00001011`

00001100
& 00001011

00001000


The result is `00001000`, which removes the rightmost set bit of `n`.

### Why This Works
- The rightmost set bit in `n` is the first bit from the right that is `1`.
- When you subtract 1 from `n`, all bits after this bit (including the bit itself) are flipped.
- When `n` and `n - 1` are ANDed together, all bits after the rightmost set bit (including the bit itself) become `0` because they are flipped and zeroed out.

### General Case
For any integer `n`, the expression `n & (n - 1)` removes the rightmost set bit. This can be useful in many scenarios, such as reducing the number of set bits in a number, checking if a number is a power of two, or performing efficient bit manipulation tasks.

## Examples

1. **Example 1:**
   - `n = 10` (binary: `00001010`)
   - `n - 1 = 9` (binary: `00001001`)
   - `n & (n - 1) = 00001010 & 00001001 = 00001000`
   - The result is `00001000`, removing the rightmost set bit.

2. **Example 2:**
   - `n = 20` (binary: `00010100`)
   - `n - 1 = 19` (binary: `00010011`)
   - `n & (n - 1) = 00010100 & 00010011 = 00010000`
   - The result is `00010000`, removing the rightmost set bit.

## Conclusion
Using `n & (n - 1)` is an efficient technique in bit manipulation to remove the rightmost set bit from a number. It takes advantage of the properties of binary subtraction and bitwise AND operations to achieve this in constant time.

