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

## What is Polymorphism?
Polymorphism is one of the four fundamental principles of Object-Oriented Programming (OOP), alongside encapsulation, inheritance, and abstraction. Polymorphism allows objects to be treated as instances of their parent class rather than their actual class. The term polymorphism means "many shapes" or "many forms." In OOP, it enables a single interface to represent different underlying forms (data types).

### Types of Polymorphism
1. **Compile-Time Polymorphism (Static Binding)**
   - Achieved through method overloading.
   - The method to be executed is determined at compile time.
   - Methods in the same class have the same name but different parameters (number, type, or both).

2. **Runtime Polymorphism (Dynamic Binding)**
   - Achieved through method overriding.
   - The method to be executed is determined at runtime.
   - A subclass provides a specific implementation of a method that is already defined in its superclass.

### Method Overloading (Compile-Time Polymorphism)
Method overloading allows multiple methods in the same class to have the same name but different parameters. It increases the readability of the program.

```java
class MathOperations {
    // Overloaded methods
    public int add(int a, int b) {
        return a + b;
    }

    public double add(double a, double b) {
        return a + b;
    }

    public int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        MathOperations math = new MathOperations();
        System.out.println(math.add(2, 3));          // Outputs 5
        System.out.println(math.add(2.5, 3.5));      // Outputs 6.0
        System.out.println(math.add(1, 2, 3));       // Outputs 6
    }
}
```

### Method Overriding (Runtime Polymorphism)
Method overriding allows a subclass to provide a specific implementation of a method that is already defined in its superclass. It enables Java to support runtime polymorphism.

```java
class Animal {
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
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
```

### Benefits of Polymorphism
1. **Flexibility**: Polymorphism allows for implementing the same method in different ways for different objects.
2. **Maintainability**: Easier to manage and maintain code as new classes can be added with minimal changes to the existing code.
3. **Extensibility**: New classes can be added to the system without affecting the existing functionality.

### Key Points
- Polymorphism is a core concept in OOP that enhances flexibility and maintainability.
- Compile-time polymorphism is achieved through method overloading.
- Runtime polymorphism is achieved through method overriding.
- Polymorphism allows one interface to be used for a general class of actions, making it easier to add new functionalities.