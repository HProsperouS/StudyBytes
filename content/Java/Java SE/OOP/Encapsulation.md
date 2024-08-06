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
description: Java SE - OOP - Encapsulation
---

## Encapsulation
---
Encapsulation is the practice of bundling the data (attributes) and the methods (functions) that manipulate that data together. The data is protected within the object, and other parts of the program can only interact with the data through authorized methods.

It make sure that "sensitive" data is hidden from users. To achieve this:
- Declare class variables/attributes as `private`
- Provide public get and set methods to access and update the value of a private variable

## Get and Set
---
`private` variables can only be accessed within the same class (an outside class has no access to it). However, it is possible to access them if we provide public **get** and **set** methods.

The get method returns the variable value, and the set method sets the value. Syntax for both is that they start with either `get` or `set`, followed by the name of the variable:
```java
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```

## Why Encapsulation?
---
- Better control of class attributes and methods
- Class attributes can be made read-only (if you only use the get method), or write-only (if you only use the set method)
- Flexible: the programmer can change one part of the code without affecting other parts
- Increased security of data