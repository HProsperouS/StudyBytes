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
description: Java SE - OOP - Super
---

## `super` Keyword
- `super` represents a reference to the superclass, used to access the superclass's properties, methods, and constructors.

1. **Accessing the superclass's properties, but not the superclass's private properties**
- Example:
```java
super.propertyName;
```

2. **Accessing the superclass's methods, but not the superclass's private methods**
- Example:
  ```java
  super.methodName(parameterList);
  ```

3. **Accessing the superclass's constructor**
- Example:
  ```java
  super(parameterList); // Must be placed in the first line of the constructor and can only appear once!
  ```
