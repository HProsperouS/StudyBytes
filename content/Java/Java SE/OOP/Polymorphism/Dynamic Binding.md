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

Java's dynamic binding mechanism refers to determining which method to call at runtime based on the actual type of the object. This feature is a key aspect of object-oriented programming and supports polymorphism.

## Static Binding vs. Dynamic Binding
- **Static Binding**: Also known as early binding, it occurs at compile-time. The compiler decides which method to call based on the reference type. This is typically used for:
  - Static methods
  - Private methods
  - Constructors
  
- **Dynamic Binding**: Also known as late binding, it occurs at runtime. The compiler cannot determine which method to call; instead, the method to be invoked is determined based on the actual object type during runtime. This applies to instance methods that can be overridden by subclasses.

## Polymorphism
Dynamic binding is closely related to polymorphism. When a parent class reference points to a child class object, the method that is called is determined by the actual object type, not the reference type. This allows the same method call to exhibit different behaviors depending on the object on which it is invoked.

## Example
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();  // Animal reference to Animal object
        Animal myDog = new Dog();        // Animal reference to Dog object
        Animal myCat = new Cat();        // Animal reference to Cat object

        myAnimal.sound();  // Outputs "Animal makes a sound"
        myDog.sound();     // Outputs "Dog barks" (Dynamic Binding)
        myCat.sound();     // Outputs "Cat meows" (Dynamic Binding)
    }
}
```

In this example, `myDog` and `myCat` are references of type `Animal`, but at runtime, Java uses `dynamic binding` to invoke the sound method of the `Dog` and `Cat` classes, rather than the `Animal` class's method.

Dynamic binding allows Java to handle objects of different types flexibly at runtime, enhancing code extensibility and maintainability.