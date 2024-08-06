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
description: Java SE - OOP - Inheritance
---

## Inheritance
---
In Java, it is possible to inherit attributes and methods from one class to another. We group the "inheritance concept" into two categories:
- subclass (child) - the class that inherits from another class
- superclass (parent) - the class being inherited from

To inherit from a class, use the extends keyword.
```java
class Vehicle {
    // protected modifier is used to make the attribute accessible in the subclasses.
    protected String brand = "Ford"; 
    public void honk() {                    
        System.out.println("Tuut, tuut!");
    }
}

class Car extends Vehicle {
    private String modelName = "Mustang";    

    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.honk();
        System.out.println(myCar.brand + " " + myCar.modelName);
    }

}
```

### The `final` Keyword
If you don't want other classes to inherit from a class, use the `final` keyword:

```java
final class Vehicle {
  ...
}

class Car extends Vehicle {
  ...
}
```
```sh
Main.java:9: error: cannot inherit from final Vehicle
class Main extends Vehicle {
                  ^
1 error)
```

### Inheritance Usage Details

1. A subclass inherits all the properties and methods from the superclass, but private properties and methods cannot be accessed directly in the subclass. They must be accessed through public methods. If the properties and methods are marked as protected, then they can be accessed directly by the subclass.

2. A subclass must call the superclass's constructor to complete the superclass's initialization.

3. When creating a subclass object, regardless of which constructor of the subclass is used, by default the no-argument constructor of the superclass will always be called. If the superclass does not provide a no-argument constructor, then the subclass constructor must use `super` to specify which constructor of the superclass should be used to complete the initialization of the superclass; otherwise, the compilation will fail.

4. If you want to call a specific constructor of the superclass, you need to explicitly call it.

5. When using `super`, it needs to be placed in the first line of the constructor.

6. `super()` and `this()` can only be placed in the first line of the constructor, so these two methods cannot coexist in one constructor.

7. All Java classes are subclasses of the Object class.

8. The call to the superclass constructor is not limited to the direct superclass but will trace back all the way to the Object class (the top-level superclass).

9. A subclass can inherit from only one superclass at most (i.e., direct inheritance), meaning that Java uses a single inheritance mechanism.

10. Inheritance should not be misused; the subclass and the superclass must satisfy the is-a logical relationship.

