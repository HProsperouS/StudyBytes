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
description: Java - Operators - Bitwise Operator - Bitwise AND.
---

## Abstract
---
- Performs an AND operation on each corresponding bit of its operands. The result bit is 1 if both corresponding bits of the operands are 1, otherwise, it is 0.
- Example: `0101 & 0011` results in `0001`.

```java
public static void main(String[] args) {
    int a = 5; // Binary representation: 0101
    int b = 3; // Binary representation: 0011
    
    int andResult = a & b; // Result: 0001 (1)

    System.out.println("a & b = " + andResult); // Output: 1
}
```

## Common Use Cases
---
### 1. Checking Odd or Even
- You can use `n & 1` to check if a number `n` is odd or even. `n & 1` is `1` if `n` is odd and `0` if n is even.
  
#### Principle of Determining Odd or Even
In binary representation:
- The least significant bit (the rightmost bit) of an even number is `0`.
- The least significant bit of an odd number is `1`.

For example:
- Even number: The binary representation of `4` is `100`, and the least significant bit is `0`.
- Odd number: The binary representation of `5` is `101`, and the least significant bit is `1`.

```java
if ((n & 1) == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```
1. `n & 1` extracts the least significant bit of `n` and performs a bitwise AND operation with `1`.
2. If `n` is even, its least significant bit is `0`, so the result of `(n & 1)` is `0`, and the code enters the if branch, printing "Even".
3. If `n` is odd, its least significant bit is `1`, so the result of `(n & 1)` is `1`, and the code enters the else branch, printing "Odd".

This method allows for a very efficient way to determine whether a number is odd or even because bitwise operations are more efficient than the modulus operation (n % 2).

### 2. Clearing the Lowest Set Bit
- You can use `n & (n - 1)` to clear the lowest set bit of an integer `n`. This is useful in counting the number of 1s in the binary representation of a number.
```java
while (n != 0) {
    n = n & (n - 1);
}
```
#### Principle of Clearing the Lowest Set Bit
To understand this, consider the binary representation of `n` and `n - 1`.
1. Binary Representation: 
   - When you subtract `1` from `n`, the rightmost `1` in `n `and all the bits to the right of it flip.
   - For example, if `n` is `10100` (which is `20` in decimal), `n - 1` will be `10011` (which is `19` in decimal).
  
2. Bitwise AND Operation:
   - Performing `n & (n - 1)` will clear the rightmost `1` in n.
   - In the example above, `10100` & `10011` will result in 10000 (which is 16 in decimal).

Let's go through the example step by step:
1. `n = 20` (binary: 10100)
2. `n - 1 = 19` (binary: 10011)
3. `n & (n - 1)`:
   - 10100
   - 10011
   - Result: 10000 (which is 16 in decimal)

The rightmost 1 in the binary representation of 20 has been cleared.

#### Practical Use
- This technique is particularly useful for **counting the number of 1s** in the binary representation of a number. Each iteration of the loop **effectively removes one 1**, so the number of iterations until n becomes 0 is equal to the number of 1s in the original binary representation of n.

```java
public static void main(String[] args) {
    int n = 20; 
    int count = 0;
    while (n != 0) {
        n = n & (n - 1);
        count++;
    }
    System.out.println("Number of 1s: " + count); // Output will be 2 for the number 20
}
```

## Example Problems on LeetCode
- [LeetCode 191 - Number of 1 Bits](https://leetcode.cn/problems/number-of-1-bits/description/)
