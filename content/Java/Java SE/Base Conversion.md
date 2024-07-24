---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - java se
Creation Date: 
Last Date: 
References: 
description: Base Conversion
---

## Convert Other Bases to Decimal
---
### Binary to Decimal 
1. Expand each binary digit from right to left according to its positional value
   - Each binary digit is multiplied by 2 raised to the power of its position index.
   - For example, for the binary number $$1101_2$$: $$1 × 2^3 + 1 × 2^2 + 0 × 2^1 + 1 × 2^0$$
2. Calculate the value of each term and sum them up
   - $$8 + 4 + 0 + 1 = 13$$

### Octal to Decimal 
1. Expand each octal digit from right to left according to its positional value
   - Each octal digit is multiplied by 8 raised to the power of its position index.
   - For example, for the binary number $$157_8$$: $$1 × 8^2 + 5 × 8^1 + 7 × 8^0$$
2. Calculate the value of each term and sum them up
   - $$64 + 40 + 7 = 111$$

### Hexadecimal to Decimal
1. Expand each hexadecimal  digit from right to left according to its positional value
   - Each hexadecimal digit is multiplied by 16 raised to the power of its position index.
   - For example, for the binary number $$1A3F_16$$: $$1 × 16^3 + A × 16^2 + 3 × 16^1 + F × 16^0$$
2. Calculate the value of each term and sum them up
   - $$4096 + 2560 + 48 + 15 = 6719$$

## Convert Other Bases to Binary
---
### Decimal to Binary
1. **Divide the decimal number by 2** and record the remainder.
2. **Update the decimal number** to the quotient obtained from the division.
3. **Repeat** steps 1 and 2 until the quotient becomes 0.
4. The binary number is the sequence of remainders read from bottom to top.

**Example Steps**

Convert the decimal number 23 to binary:

   1. Divide 23 by 2: 
      - $$23÷2=11, remainder=1$$
   2. Divide 11 by 2:
      - $$11÷2=5, remainder=1$$
   3. Divide 5 by 2:
      - $$5÷2=2, remainder=1$$
   4. Divide 2 by 2:
      - $$2÷2=1, remainder=0$$
   5. Divide 1 by 2:
      - $$1÷2=0, remainder=1$$

Reading the remainders from bottom to top, we get the binary number: 
   - $$23_10 = 10111_2$$

### Octal to Binary
1. **Convert each octal digit to its 3-bit binary equivalent**
   - Each octal digit (0-7) can be represented as a 3-bit binary number.
   - For example, the octal digit 7 is 111 in binary, 5 is 101, etc.
2. **Concatenate the binary equivalents**
   - Combine the binary representations of each octal digit to get the full binary number.

**Conversion Table**:
| Octal | Binary |
|-------|--------|
| 0     | 000    |
| 1     | 001    |
| 2     | 010    |
| 3     | 011    |
| 4     | 100    |
| 5     | 101    |
| 6     | 110    |
| 7     | 111    |

**Example Steps**:

Convert the octal number $$745_8$$ to binary:

1. Split the octal number into individual digits: 7, 4, 5.
2. Convert each digit to its binary equivalent:
   - 7 → 111
   - 4 → 100
   - 5 → 101
3. Concatenate these binary numbers: $$111100101_2$$

### Hexadecimal to Binary
1. **Convert each hexadecimal digit to its 4-bit binary equivalent**:
   - Each hexadecimal digit (0-9, A-F) can be represented as a 4-bit binary number.
   - For example, the hexadecimal digit F is 1111 in binary, A is 1010, etc.

2. **Concatenate the binary equivalents**:
   - Combine the binary representations of each hexadecimal digit to get the full binary number.

**Conversion Table**:
| Hexadecimal | Binary  |
|-------------|---------|
| 0           | 0000    |
| 1           | 0001    |
| 2           | 0010    |
| 3           | 0011    |
| 4           | 0100    |
| 5           | 0101    |
| 6           | 0110    |
| 7           | 0111    |
| 8           | 1000    |
| 9           | 1001    |
| A           | 1010    |
| B           | 1011    |
| C           | 1100    |
| D           | 1101    |
| E           | 1110    |
| F           | 1111    |

**Example Steps**:

Convert the hexadecimal number $$2A3E_{16}$$ to binary:

1. Split the hexadecimal number into individual digits: 2, A, 3, E.
2. Convert each digit to its binary equivalent:
   - 2 → 0010
   - A → 1010
   - 3 → 0011
   - E → 1110
3. Concatenate these binary numbers: $$0010101000111110_2$$

## Convert Other Bases to Octal
---
### Decimal to Octal
1. **Divide the decimal number by 8** and record the remainder.
2. **Update the decimal number** to the quotient obtained from the division.
3. **Repeat** steps 1 and 2 until the quotient becomes 0.
4. The binary number is the sequence of remainders read from bottom to top.

### Binary to Octal


### Hexadecimal to Octal


## Convert Other Bases to Hexadecimal
---

