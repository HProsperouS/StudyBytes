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
description: Java - Operators - Bitwise Operator - Bitwise XOR.
---

## Abstract
---
- Performs an exclusive OR operation on each corresponding bit of its operands. The result bit is 1 if the corresponding bits of the operands are different (one is 1, the other is 0).
- Example: `0101 ^ 0011` results in `0110`.

```java
public static void main(String[] args) {
    int a = 5; // Binary representation: 0101
    int b = 3; // Binary representation: 0011
    
    int xorResult = a ^ b; // Result: 0110 (6)
    
    System.out.println("a ^ b = " + xorResult); // Output: 6
}
```

## Common Use Cases
---
### 1. Swapping Two Numbers
- You can use XOR to swap two numbers without using a temporary variable.
```java
a = a ^ b;
b = a ^ b;
a = a ^ b;
```

### 2. Finding the Unique Number
- In an array where every number appears twice except for one, XOR can find the unique number in linear time.

```java
int unique = 0;
for (int num : nums) {
    unique ^= num;
}
```

### 3. Calculating Hamming Distance
- XOR can be used to calculate the Hamming distance between two integers, which is the number of differing bits.

```java
int x = 5; // 0101
int y = 3; // 0011
int hammingDistance = Integer.bitCount(x ^ y); // 2
```

## Example Problems on LeetCode
- [LeetCode 461 - Hamming Distance](https://leetcode.cn/problems/hamming-distance/description/)
- [LeetCode 136 - Single Number](https://leetcode.cn/problems/single-number/description/)


