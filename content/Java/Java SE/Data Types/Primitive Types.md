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
description: Java Basic - Primitive Types
---

## Abstract
---
Data types are divided into two groups:
- Primitive data types - includes byte, short, int, long, float, double, boolean and char
- Non-primitive data types - such as String, Arrays and Classes

## Primitive Data Types
---
- A primitive data type specifies the size and type of variable values, and it has no additional methods.

There are eight primitive data types in Java:

| Data Type | Size    | Description                                 |
|-----------|---------|---------------------------------------------|
| `byte`    | 1 byte  | Stores whole numbers from -128 to 127        |
| `short`   | 2 bytes | Stores whole numbers from -32,768 to 32,767  |
| `int`     | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647 |
| `long`    | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| `float`   | 4 bytes | Stores fractional numbers                    |
| `double`  | 8 bytes | Stores fractional numbers                    |
| `char`    | 2 bytes | Stores a single 16-bit Unicode character     |
| `boolean` | 1 byte  | Stores `true` or `false`                    |

>[!note] Use float or double?
> The **precision** of a floating point value indicates how many digits the value can have after the decimal point. The precision of `float` is only six or seven decimal digits, while double variables have a precision of about 15 digits. Therefore it is safer to use `double` for most calculations.

## Float pitfalls
---
 ```java
    double num1 = 2.7;
    double num2 = 8.1 / 3;
    System.out.println(num1); //2.7
    System.out.println(num2); //2.6999999999999997
```
### Root Cause
- Floating-point numbers are represented in computers according to the IEEE 754 standard. This method of representation cannot precisely represent certain decimal numbers, such as 2.7, in a binary system. Many decimal fractions convert to repeating binary fractions, and the computer can only store and operate on approximate values. This leads to precision errors during calculations and output.

### Solution
- If higher precision calculations are needed, the `BigDecimal` class can be used instead of the `double` type. The BigDecimal class provides arbitrary precision calculations.

```java
import java.math.BigDecimal;
BigDecimal num1 = new BigDecimal("2.7");
BigDecimal num2 = new BigDecimal("8.1").divide(new BigDecimal("3"), 10, RoundingMode.HALF_UP);

System.out.println(num1); // 2.7
System.out.println(num2); // 2.7
```

- When comparing whether two numbers are equal, the absolute value of the difference between the two numbers should be used to determine within a certain precision range
```java
double num1 = 2.7;
double num2 = 8.1 / 3;
System.out.println(num1); //2.7
System.out.println(num2); //2.6999999999999997

//Wrong Method
if(num1 == num2){
    System.out.println("Equal");
}

//Correct Method
if(Math.abs(num1-num2) < 0.00000001){
    System.out.println("Equal2");
}
```