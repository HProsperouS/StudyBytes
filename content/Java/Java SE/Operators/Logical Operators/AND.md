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
description: Java - Operators - Logical Operator - AND.
---

## Abstract
---
- In Java, there are two types of AND operators: the logical AND (`&`) and the short-circuit AND (`&&`). 
- Logical AND can be used for boolean logic and bitwise operations on integers, so it is also known as [[Bitwise AND]].

They differ in how they evaluate their operands:
1. Logical AND (`&`):
   - Performs a bitwise AND operation on two boolean operands. Both operands are evaluated, even if the first operand is `false`.
   - Example: `a & b`
2. Short-circuit AND (`&&`):
   - If the first operand is `false`, the second operand is not evaluated. This can improve efficiency and prevent potential errors (e.g., avoiding method calls on `null` objects).
   - Example: `a && b`

### Example Code
```java
public class AndOperatorsExample {
    public static void main(String[] args) {
        boolean a = true;
        boolean b = false;

        // Logical AND operator
        System.out.println("a & b: " + (a & b)); // false

        // Short-circuit AND operator
        System.out.println("a && b: " + (a && b)); // false

        // Logical AND operator, does not short-circuit
        try {
            boolean result1 = false & (5 / 0 > 1); // This line will throw an exception because 5 / 0 is evaluated
            System.out.println("result1: " + result1);
        } catch (ArithmeticException e) {
            System.out.println("ArithmeticException caught: " + e.getMessage());
        }

        // Short-circuit AND operator, will short-circuit
        boolean result2 = false && (5 / 0 > 1); // This line will not throw an exception because && short-circuits
        System.out.println("result2: " + result2); // false
    }
}
```