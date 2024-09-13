
# Object-Oriented Programming (OOP) in Java

## Introduction to OOP
Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes to structure software in a modular way. It allows for better data management, code reuse, and abstraction of complex systems.

## Key Concepts in OOP

### 1. Class
A **Class** is a blueprint for creating objects. It defines a type of object according to the data and methods it will contain.
- **Example**: A class `Car` defines a template for car objects, including properties like `color` and `year`, and methods like `drive()`.
    ```java
    public class Car {
        private String color;
        private int year;

        public Car(String color, int year) {
            this.color = color;
            this.year = year;
        }

        public void drive() {
            System.out.println("Driving the car");
        }
    }
    ```

### 2. Object
An **Object** is an instance of a class. It has state (attributes) and behavior (methods). Objects are created from classes.
- **Example**: Creating an object of the `Car` class.
    ```java
    Car myCar = new Car("Red", 2022);
    myCar.drive();
    ```

### 3. Inheritance
**Inheritance** allows a class to use properties and methods of another class. It promotes code reuse and establishes a relationship between classes.
- **Example**: `ElectricCar` inherits from `Car`, adding specific properties like `batteryLife`.
    ```java
    public class ElectricCar extends Car {
        private int batteryLife;

        public ElectricCar(String color, int year, int batteryLife) {
            super(color, year);
            this.batteryLife = batteryLife;
        }
    }
    ```

### 4. Polymorphism
**Polymorphism** allows a single interface to represent different underlying forms (data types). It is mainly used for method overloading and method overriding.
- **Example**: Using a method in different forms.
    ```java
    Car myCar = new ElectricCar("Blue", 2023, 500);
    myCar.drive(); // Calls the overridden method in ElectricCar
    ```

### 5. Encapsulation
**Encapsulation** is the wrapping of data (variables) and code (methods) together into a single unit (class). It restricts direct access to some of an object's components.
- **Example**: Using getters and setters.
    ```java
    public class Person {
        private String name;
        private int age;

        public String getName() {
            return name;
        }

        public void setName(String name) {
            this.name = name;
        }
    }
    ```

### 6. Abstraction
**Abstraction** hides the complex reality while exposing only the necessary parts. It can be achieved using abstract classes and interfaces.
- **Example**: An abstract class `Animal` with an abstract method `sound()`.
    ```java
    public abstract class Animal {
        public abstract void sound();
    }

    public class Dog extends Animal {
        public void sound() {
            System.out.println("Woof");
        }
    }
    ```

## Benefits of OOP
- **Modularity**: Code is organized into objects and classes.
- **Reusability**: Classes and objects can be reused across programs.
- **Scalability**: Easier to manage larger codebases.
- **Maintainability**: Clear structure improves code maintenance.
- **Abstraction**: Simplifies complex real-world problems.

## Practical Application of OOP in Java
- **Creating User Interfaces**: Using objects to represent different UI components.
- **Building Games**: Representing characters, environments, and events as objects.
- **Managing Databases**: Mapping database records to objects for easy manipulation.


## Simple Diagram

```
+------------------+
|      Class       |
|------------------|
| - attributes     |
| + methods()      |
+------------------+
        |
        |
    Inheritance
        |
        v
+------------------+
|   Subclass       |
|------------------|
| - new attributes |
| + new methods()  |
+------------------+
```

## Summary

- **OOP** is a programming paradigm that uses objects and classes.
- It encourages modularity, code reusability, and a clear structure.
- The four main principles are **Inheritance, Polymorphism, Encapsulation,** and **Abstraction**.
