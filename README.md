# Classes in C#

## Table of Contents
1. [Introduction](#introduction)
2. [Defining a Class](#defining-a-class)
3. [Creating Objects](#creating-objects)
4. [Access Modifiers](#access-modifiers)
5. [Fields and Properties](#fields-and-properties)
6. [Methods](#methods)
7. [Constructors](#constructors)
8. [Static Members](#static-members)
9. [Inheritance](#inheritance)
10. [Polymorphism](#polymorphism)
11. [Abstract Classes](#abstract-classes)
12. [Interfaces](#interfaces)
13. [Encapsulation](#encapsulation)
14. [Key Takeaways](#key-takeaways)
15. [Additional Resources](#additional-resources)

---

## Introduction
Classes are one of the fundamental building blocks of object-oriented programming (OOP) in C#. A class is a blueprint for creating objects, providing initial values for fields, and implementing behavior through methods. Understanding classes is crucial to writing effective and reusable code in C#.

---

## Defining a Class
To define a class in C#, use the `class` keyword followed by the class name:

```csharp
public class Person
{
    // Fields, properties, methods, etc.
}
```

### Example:
```csharp
public class Person
{
    public string Name;
    public int Age;
}
```

---

## Creating Objects
You can create an object from a class using the `new` keyword:

```csharp
Person person = new Person();
person.Name = "John";
person.Age = 30;
```

---

## Access Modifiers
Access modifiers define the visibility of class members. Common access modifiers include:
- `public`: Accessible from anywhere.
- `private`: Accessible only within the class.
- `protected`: Accessible within the class and derived classes.
- `internal`: Accessible within the same assembly.

### Example:
```csharp
public class Person
{
    private string Name;
    protected int Age;
    public void DisplayInfo()
    {
        Console.WriteLine($"Name: {Name}, Age: {Age}");
    }
}
```

---

## Fields and Properties
Fields store data, while properties provide controlled access to them. Properties use `get` and `set` accessors.

### Example:
```csharp
public class Person
{
    private string name;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}
```

---

## Methods
Methods define the actions a class can perform.

### Example:
```csharp
public class Calculator
{
    public int Add(int a, int b)
    {
        return a + b;
    }
}
```

---

## Constructors
Constructors initialize objects when they are created. They share the same name as the class.

### Example:
```csharp
public class Person
{
    public string Name;
    public int Age;

    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```

---

## Static Members
Static members belong to the class rather than any object.

### Example:
```csharp
public class Calculator
{
    public static int Add(int a, int b)
    {
        return a + b;
    }
}
```

---

## Inheritance
Inheritance allows a class to derive from another class, inheriting its members.

### Example:
```csharp
public class Animal
{
    public void Eat()
    {
        Console.WriteLine("Eating...");
    }
}

public class Dog : Animal
{
    public void Bark()
    {
        Console.WriteLine("Barking...");
    }
}
```

---

## Polymorphism
Polymorphism enables methods to be overridden or used in different ways.

### Example:
```csharp
public class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal speaks");
    }
}

public class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Dog barks");
    }
}
```

---

## Abstract Classes
Abstract classes cannot be instantiated and may contain abstract methods that must be implemented by derived classes.

### Example:
```csharp
public abstract class Shape
{
    public abstract double GetArea();
}

public class Circle : Shape
{
    public double Radius;

    public Circle(double radius)
    {
        Radius = radius;
    }

    public override double GetArea()
    {
        return Math.PI * Radius * Radius;
    }
}
```

---

## Interfaces
Interfaces define a contract that classes must implement.

### Example:
```csharp
public interface IMovable
{
    void Move();
}

public class Car : IMovable
{
    public void Move()
    {
        Console.WriteLine("Car is moving");
    }
}
```

---

## Encapsulation
Encapsulation is the practice of bundling data and methods together and restricting access to them.

### Example:
```csharp
public class Account
{
    private double balance;

    public void Deposit(double amount)
    {
        if (amount > 0)
        {
            balance += amount;
        }
    }

    public double GetBalance()
    {
        return balance;
    }
}
```

---

## Key Takeaways
- Classes are the foundation of OOP in C#.
- Use access modifiers to control visibility.
- Fields, properties, and methods define the structure and behavior of a class.
- Master concepts like inheritance, polymorphism, and encapsulation to build reusable and maintainable code.

---

## Additional Resources
- [Microsoft C# Documentation](https://learn.microsoft.com/en-us/dotnet/csharp/)
- [C# Programming Guide](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/)
- [OOP Principles in C#](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/tutorials/oop)

---

Happy Coding! 🎉

