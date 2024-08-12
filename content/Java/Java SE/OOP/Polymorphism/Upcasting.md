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
description: Java SE - OOP - Polymorphism
---

## What is Upcasting
Upcasting refers to the process of assigning a subclass object to a superclass reference variable. In Java, since a subclass object can be treated as an instance of its superclass, this type of conversion happens implicitly without requiring an explicit cast.

### 1. How Upcasting Works
When a subclass object is assigned to a reference of its superclass type, upcasting occurs. In this situation, the superclass reference can access overridden methods in the subclass but cannot access methods or fields specific to the subclass (i.e., the compiler only sees the superclass part).

```java
Parent parent = new Child(); // Upcasting
```

### 2. Purpose of Upcasting
- **Polymorphism**: Upcasting allows a superclass reference to point to objects of multiple subclass types, thus enabling polymorphism. For example, a method can accept a parameter of the superclass type, allowing it to work with any subclass object.
- **Unified Interface**: Upcasting enables a uniform way to operate on different subclass objects using a superclass reference.

### 3. Example Code
```java
class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Dog barks");
    }

    void fetch() {
        System.out.println("Dog fetches the ball");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog(); // Upcasting
        myAnimal.makeSound(); // Output: Dog barks
        // myAnimal.fetch(); // Compilation error, as the superclass reference cannot call methods specific to the subclass
    }
}
```

### 4. Key Points Summary 
- **Automatic Conversion**: Upcasting happens automatically, without the need for explicit casting.
- **Access Limitation**: After upcasting, the superclass reference can only access methods declared in the superclass. Subclass-specific methods are inaccessible unless downcasting is performed.
- **Polymorphism**: Upcasting allows a superclass reference to point to different subclass objects, enabling polymorphic behavior.

### 5. Role in Polymorphism
Upcasting allows us to write more general and flexible code. For instance, you can write a method that accepts a superclass type parameter and can operate on any subclass object, eliminating the need to write multiple overloaded methods.

### Extended Example
```java
public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog(); // Upcasting
        testAnimal(myAnimal); // Can handle objects of any subclass of Animal
    }

    public static void testAnimal(Animal animal) {
        animal.makeSound();
    }
}
```
This shows how upcasting can be used in method parameters, allowing different subclass objects to be passed and the correct method to be called, thus achieving polymorphism and reusability in the code.


