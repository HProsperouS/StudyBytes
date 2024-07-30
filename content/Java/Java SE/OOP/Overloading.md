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
description: Java SE - OOP - Overloading
---

## Abstract
---
- Overloading in Java refers to the ability to define multiple methods with the same name but with different parameters (different type or number of parameters) within the same class. 
- This is a form of polymorphism and allows methods to perform different tasks based on the input parameters.

### Key Points of Method Overloading in Java
1. **Same Method Name**: All overloaded methods must have the same name.
2. **Different Parameters**: Overloaded methods must differ in the number or type of parameters. They can also differ in both.
3. **Return Type**: The return type can be different, but it alone does not constitute overloading. The method signature (method name and parameter list) must be different.
4. **Compile-Time Polymorphism**: Overloading is resolved at compile time, hence it is also known as compile-time polymorphism or static binding.

```java
public class MathOperations {
    // Method to add two integers
    public int add(int a, int b) {
        return a + b;
    }

    // Overloaded method to add three integers
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // Overloaded method to add two double values
    public double add(double a, double b) {
        return a + b;
    }
}
```