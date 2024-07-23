---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - java
Creation Date: 
Last Date: 
References: 
description: Java - Operators - Arithmetic Operator - Modulus.
---

## Abstract
---
- The modulus operator in Java is represented by the percentage symbol `%`.	
- It returns the remainder of a division operation. 

### Examples
```java
public static void main(String[] args) {
    System.out.println(10 % 3); // Ouput: 1
    System.out.println(-10 % 3); // Output: -1
    System.out.println(10 % -3); // Outpur: 1
    System.out.println(-10 % -3); // Output: -1
}
```
>[!note] The result of the modulus operation takes the sign of the dividend.
> 1. -10 % 3 = -1 
> 2. -10 % -3 = -1
> The essence of % can be seen in a formula: a % b = a - a/b * b
