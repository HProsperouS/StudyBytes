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
description: Java Basic - Java Type Casting
---

## Abstract
---
- Type casting is when you assign a value of one primitive data type to another type.
- In Java, there are two types of casting:
  - Widening Casting (automatically) - converting a smaller type to a larger type size `byte` -> `short` -> `char` -> `int` -> `long` -> `float` -> `double`
  - Narrowing Casting (manually) - converting a larger type to a smaller size type `double` -> `float` -> `long` -> `int` -> `char` -> `short` -> `byte`

## Widening Casting
---
- Widening casting is done automatically when passing a smaller size type to a larger size type:
```java
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```

## Narrowing Casting
---
- Narrowing casting must be done manually by placing the type in parentheses () in front of the value:
```java
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```
>[!caution] Narrow Casting in Java can cause overflow and loss of precision. 
> Narrow casting, also known as explicit casting, involves converting a larger data type to a smaller data type. 
> 1. Loss of Precision: Converting `double` to `int`
> ```java
> public static void main(String[] args) {
>   double doubleValue = 9.78;
>   int intValue = (int) doubleValue; 
>   System.out.println("Original double value: " + doubleValue);
>   System.out.println("Converted int value: " + intValue); 
> }
> 
> ```
> ```
> Original double value: 9.78
> Converted int value: 9
> ```
> 2. Overflow: Converting int to byte
> ```java
> public static void main(String[] args) {
>   int intValue = 130;
>   byte byteValue = (byte) intValue; 
>   System.out.println("Original int value: " + intValue);
>   System.out.println("Converted byte value: " + byteValue); 
> }
> ```
> ```arduino
> Original int value: 130
> Converted byte value: -126
> ```
