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
description: Java - Operators - Bitwise Operator - Bitwise OR.
---

## Abstract
---
- Performs an OR operation on each corresponding bit of its operands. The result bit is 1 if at least one of the corresponding bits of the operands is 1.
- Example: `0101 | 0011` results in `0111`.

```java
public static void main(String[] args) {
    int a = 5; // Binary representation: 0101
    int b = 3; // Binary representation: 0011
    
    int orResult = a | b;  // Result: 0111 (7)
    
    System.out.println("a | b = " + orResult);  // Output: 7
}
```

## Common Use Cases
---
### 1. Setting a Specific Bit
- You can use `n | (1 << k)` to set the `k-th` bit of an integer `n` to `1`. This is common in bit manipulation tasks.
```java
int result = n | (1 << k);
```

### 2. Combining Permissions
- In permission management, bitwise OR is used to combine multiple permission flags.
```java
int readPermission = 1;   // 0001
int writePermission = 2;  // 0010
int executePermission = 4; // 0100
int allPermissions = readPermission | writePermission | executePermission; // 0111
```

