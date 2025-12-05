# Day 1

# 1. what is c#? What is difference b/w c# and .net.

# .Net
.Net is a cross-plateform,open-source developer plateform form building many times of applications,including Web,Mobile,Destop and Games.
   It Provides a set of tools languages (like C#,VB.net and C#) and libraries to create robust Applications.
# C#
C# is a modern, object-oriented programming language developed by Microsoft. 
It is a general-purpose language that runs on the .NET platform, enabling the creation of various applications across different environments.



| **C#**                                    | **.NET**                                                    |
| ----------------------------------------- | ----------------------------------------------------------- |
| C# is a **programming language**.         | .NET is a **software development framework/platform**.      |
| Used to write code.                       | Provides runtime, libraries, and tools to run C# code.      |
| Syntax similar to Java/C++.               | Platform that supports multiple languages (C#, VB.NET, F#). |
| Only a language, cannot run without .NET. | Helps compile, run, and manage C# programs.                 |

# 2️⃣ What is OOPS? What are the main concepts of OOPS?
What is OOPS?

OOPS (Object-Oriented Programming System) is a programming methodology that uses objects and classes to structure programs.
It helps developers write modular, reusable, and maintainable code.

Main Concepts of OOPS
🔒 1. Encapsulation

Binding data and methods together and protecting them from unauthorized access.
Example: Using private fields with public getters/setters.

🧩 2. Abstraction

Showing only essential features while hiding complex details.
Example: Interfaces, abstract classes.

🧬 3. Inheritance

A class can inherit properties and methods from another class.
Example: Car inherits from Vehicle.

🎭 4. Polymorphism

"One name, many forms" — the same method behaves differently depending on context.

Method Overloading – same method name, different parameters

Method Overriding – same method name in base and derived class

3️⃣ What are the advantages of OOPS?

Reusability – Reuse code using inheritance

Maintainability – Easier to modify and manage

Security – Encapsulation protects data

Flexibility – Polymorphism allows extensibility

Modularity – Breaks complex problems into simpler modules

Higher Productivity – Faster development using reusable components

4️⃣ What are the limitations of OOPS?

Steep Learning Curve – Concepts like inheritance or abstraction can be difficult

More Memory Usage – Object creation consumes memory

Slower for Simple Tasks – Procedural programming can be faster

Over-Engineering – Unnecessary classes/objects may complicate design

Not suitable for all problems – Example: low-level system or real-time programming

5️⃣ What are Classes and Objects?
Class

A class is a blueprint or template used to create objects.
It defines properties (data) and methods (actions).

Example:
class Car
{
    public string Color;
    public void Start() {}
}

Object

An object is an instance of a class.
It represents a real-world entity.

Example:
Car myCar = new Car();

6️⃣ Types of Classes in C#
1. Concrete Class

A normal class that can be instantiated.

class Student { }

2. Abstract Class

Cannot be instantiated

Used to define shared behavior

Can contain abstract + non-abstract members

3. Sealed Class

Cannot be inherited

Used to prevent further extension

4. Static Class

Contains only static members

Cannot create objects

Used for helper/utility methods

Example: Math class

5. Partial Class

Class definition is split across multiple files

Useful for large classes

6. Nested Class

A class declared inside another class

Helps group related classes

7. Generic Class

Works with any data type using <T>

Example:

List<T>


If you want, I can add code samples, diagrams, or convert this into a PDF for interview revision.




