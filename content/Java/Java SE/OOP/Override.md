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
description: Java SE - OOP - Overide
---

## What is Method Overriding?
Method overriding in Java occurs when a subclass provides a specific implementation of a method that is already defined by its superclass. The overridden method in the subclass should have the same name, return type, and parameters as the method in the superclass.

## Rules for Method Overriding
1. **Same Method Signature**: The method in the subclass must have the same name, return type, and parameter list as the method in the superclass.
2. **Access Level**: The access level of the overriding method cannot be more restrictive than the overridden method in the superclass.
   - For example, if the superclass method is `public`, the subclass method cannot be `protected` or `private`.
3. **Instance Methods**: Only instance methods can be overridden. Static methods cannot be overridden but can be re-declared.
4. **@Override Annotation**: It is a good practice to use the `@Override` annotation to indicate that a method is being overridden. This helps catch errors if the method signatures do not match.

## Why Use Method Overriding?
- **Polymorphism**: Method overriding is a key feature of polymorphism in Java. It allows a subclass to provide a specific implementation of a method that is already defined by its superclass.
- **Runtime Polymorphism**: Overriding allows Java to support runtime polymorphism (or dynamic method dispatch), where the method to be executed is determined at runtime.

## Example of Method Overriding

```java
class Animal {
    // Method in the superclass
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    // Overriding the makeSound method in the subclass
    @Override
    public void makeSound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal(); // Animal reference and object
        Animal myDog = new Dog(); // Animal reference but Dog object

        myAnimal.makeSound(); // Calls the method in Animal class
        myDog.makeSound(); // Calls the overridden method in Dog class
    }
}