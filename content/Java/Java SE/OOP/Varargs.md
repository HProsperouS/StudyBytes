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
description: Java SE - OOP - variable-length arguments
---

## Abstract
--- 
- Varargs (variable-length arguments) allow you to pass a variable number of arguments to a method. 
- This feature simplifies the creation of methods that need to accept a flexible number of arguments, eliminating the need to define multiple overloaded methods for different numbers of parameters.

### Key Points of Varargs
1. **Syntax**: The varargs parameter is defined using an ellipsis (...) followed by the type and parameter name. For example, int... numbers allows the method to accept zero or more int values.
2. **Single Varargs Parameter**: A method can have only one varargs parameter, and it must be the last parameter in the method's parameter list.
3. **Array Representation**: Inside the method, the varargs parameter is treated as an array.

```java
public class VarargsExample {
    // Method with varargs parameter
    public static int sum(int... numbers) {
        int sum = 0;
        for (int num : numbers) {
            sum += num;
        }
        return sum;
    }

    public static void main(String[] args) {
        System.out.println(sum(1, 2, 3));       // Output: 6
        System.out.println(sum(1, 2, 3, 4, 5)); // Output: 15
        System.out.println(sum());              // Output: 0
    }
}
```