# 1️⃣ What are the types of classes in C#?

C# provides different kinds of classes for different purposes.

1. Concrete Class
A normal class that we can create objects from.

2. Abstract Class
We cannot create an object of this class.
It is used as a base class and may have incomplete methods.

3. Sealed Class
This class cannot be inherited.
It is used when we want to stop other classes from extending it.

4. Static Class
This class contains only static members.
We cannot create objects of this class.
Mostly used for helper or utility functions.

5. Partial Class
A single class divided into multiple files.
Used to manage large classes easily.

6. Nested Class
A class written inside another class.
Used when classes are closely related.

7. Generic Class
A class that can work with any data type using <T>.
Example: List<T>

# 2️⃣ Is it possible to prevent object creation of a class in C#?

Yes, we can prevent object creation in three ways:

1. Make the class abstract
Abstract classes cannot be directly created.

2. Use a private constructor
If the constructor is private, no one can create the object from outside.

3. Make the class static
Static classes cannot have objects at all.

# 3️⃣ What is Property?

A property is a member in C# that is used to get and set the value of a private field.

It helps in controlling how data is accessed.
It looks like a variable but works like a method internally.

Example:

public string Name { get; set; }

# 4️⃣ What is the difference between Property and Function?

Property

Used to get or set data.

Accessed like a variable.

Internally uses get and set.

Function (Method)

Used to perform actions or logic.

Called like a normal method.

Can take parameters and return values.

# 5️⃣ What are Namespaces?

A namespace is a way to group related classes and avoid name conflicts.
It helps in organizing code properly.

Example:

namespace Project.Services
{
    class UserService { }
}


To use the namespace:

using Project.Services;

# 6️⃣ What is Inheritance? When to use Inheritance?

Inheritance is a feature where one class (child) can use the properties and methods of another class (parent).

We use inheritance when:

We want to reuse code.

We want to define common behavior in a base class.

We want to reduce duplication.

Example:
A Car class can inherit from a Vehicle class.

# 7️⃣ What are the different types of Inheritance?

C# supports the following types:

1. Single Inheritance
One parent, one child.

2. Multilevel Inheritance
Parent → Child → Grandchild.

3. Hierarchical Inheritance
One parent, multiple children.

4. Multiple Inheritance (not supported by classes)
But C# supports it using interfaces.

# 8️⃣ Does C# support Multiple Inheritance? How can you implement it?

C# does not allow a class to inherit from more than one class.
But C# does allow a class to implement multiple interfaces.

Example:

class MyClass : IA, IB
{
}


This is the way to implement multiple inheritance in C#.

# 9️⃣ How to prevent a class from being inherited?

We can stop inheritance in two ways:

1. Using sealed keyword
A sealed class cannot be inherited.

2. Sealing a method
A method can be sealed so it cannot be overridden again.
