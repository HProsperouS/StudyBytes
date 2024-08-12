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

## What is Downcasting
Downcasting in Java is the process of converting a reference of a superclass type back to a reference of a subclass type. Unlike upcasting, downcasting is not automatic and requires an explicit cast.

## When is Downcasting Used?
Downcasting is used when you have a reference of a superclass type, but you know that the actual object is of a subclass type, and you want to access methods or fields that are specific to that subclass.

## How Downcasting Works
To perform downcasting, you explicitly cast the superclass reference to the subclass type. This allows you to access the subclass-specific methods and fields.

**Example of Downcasting**
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
        
        // Downcasting
        Dog myDog = (Dog) myAnimal; 
        myDog.fetch(); // Output: Dog fetches the ball
    }
}
```

**Key Points about Downcasting**
- **Explicit Casting**: Unlike upcasting, downcasting requires an explicit cast `(Subclass)`.
- **ClassCastException**: If you try to downcast to the wrong type (i.e., a type that the object is not an instance of), a `ClassCastException` will be thrown at runtime.
- **Instanceof Check**: To avoid `ClassCastException`, it is good practice to check the type using the `instanceof` operator before performing downcasting.

**Example with `instanceof`**
```java
if (myAnimal instanceof Dog) {
    Dog myDog = (Dog) myAnimal;
    myDog.fetch();
} else {
    System.out.println("The object is not a Dog.");
}
```

### Summary 
- **Downcasting**: Converts a reference of a superclass type to a reference of a subclass type, allowing access to subclass-specific methods and fields.
- **Usage**: It’s used when you know the object is actually of the subclass type.
- **Risks**: Downcasting can lead to ClassCastException if not done carefully, so always use instanceof to check the type before downcasting.