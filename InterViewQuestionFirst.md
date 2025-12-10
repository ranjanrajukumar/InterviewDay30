# 1. How many Classes in C#?Describe
# 2. What Difference B/w Abstract Class and Interface 
# 3. Encapsulation ? Real-Time  Seconario?
# 4. Use A Singloton Design Pattern Create A structure 
  Employee {
      Name,
     DOB,
      Address,
     Gender
  }
# 5. MSSQL  = and like keyword and difference
# 6. == and .Equal()



# #️⃣ 1. How Many Classes in C#? Describe

In C#, there is no fixed count of classes. Instead, C# provides different types of classes based on purpose and usage. Each type supports various object-oriented features like inheritance, abstraction, or encapsulation.

Types of Classes in C# (Description)
1. Concrete Class

A normal class used to create objects. It contains full implementation and represents real-world entities like Employee, Product, etc.

2. Abstract Class

A partially implemented class. It may contain abstract members that derived classes must implement. Cannot be instantiated. Used for creating base frameworks.

3. Sealed Class

A class that cannot be inherited. Used for security, performance optimization, and preventing modification of behavior.

4. Static Class

A class that cannot be instantiated. Contains only static members. Used for common utility or helper functions.

5. Partial Class

A single class divided into multiple files. Useful for large codebases where multiple developers contribute to the same class.

6. Nested Class

A class declared inside another class. Used for grouping helper classes and hiding implementation details.

# #️⃣ 2. Difference Between Abstract Class and Interface
Abstract Class

A base class containing partial implementation.

Can include fields, constructors, and fully implemented methods.

Can define default behavior.

Supports single inheritance.

Used when classes share a common identity or behavior.

Interface

A contract that defines “what a class must do.”

Cannot have fields or constructors.

All methods are abstract by default.

Supports multiple inheritance.

Used for capabilities like ISaveable, IComparable, IFlyable.

Conceptual Difference

Abstract Class → “What it IS” (base entity, common structure).

Interface → “What it CAN DO” (capability or behavior).

# #️⃣ 3. Encapsulation – Describe with Real-Time Scenario
Definition

Encapsulation is the process of hiding internal details of a class and exposing only necessary functionality. It protects data by restricting direct access using private fields and public methods or properties.

Purpose

Protect sensitive data

Prevent misuse or invalid changes

Maintain object integrity

Provide controlled access

Real-Time Scenario (Bank Account)

A bank account’s balance must not be directly changed by external users.
If balance were public, anyone could set:

balance = 1,00,00,000

Instead, the balance is kept private. Only methods like Deposit, Withdraw, and CheckBalance can modify or display it. These methods enforce validation and security.

Encapsulation ensures that the internal state remains safe and controlled.

# #️⃣ 4. Singleton Design Pattern – Describe Using Employee Structure
Definition

Singleton is a creational design pattern ensuring only one instance of a class exists in the entire application. It provides a global access point to that instance.

Why Singleton Is Used

Shared configuration

Applying global settings

Logging

Database connection management

Caching

How Singleton Works (Theory)

The constructor is private, so objects cannot be created directly.

A static instance variable stores the single allowed object.

A public method returns this single instance to all consumers.

Applying Singleton to the Employee Structure

If we ensure that only one Employee object exists throughout the application (such as a logged-in user profile), then all modules will read the same employee data.

This ensures:

Consistent information

No duplicate objects

Global access to the same instance

# #️⃣ 5. MSSQL — Describe = vs LIKE Keyword
= Operator

Used for exact value matching.

Retrieves rows where the column matches the specified value exactly.

Fast because it uses indexes effectively.

Used for numbers, exact names, IDs, dates.

Example:
Name = 'Raju' → finds only the exact match.

LIKE Operator

Used for pattern matching using wildcards.

Common wildcards:

% = zero or more characters

_ = exactly one character

Useful in search functionality and filtering.

May be slower because wildcard searches reduce index use.

Example:
Name LIKE 'Raj%' → finds Raj, Raju, Rajesh, etc.

Conceptual Difference
Feature	=	LIKE
Purpose	Exact match	Pattern match
Speed	Faster	Slower
Use Case	Strict filtering	Searching
Wildcards	No	Yes
# #️⃣ 6. Difference Between == and .Equals() (Theoretical Description)
== Operator

Compares values for value types.

Compares memory references for reference types (unless overridden).

Commonly used for primitives like int, bool, char.

Meaning:

For reference types, == checks if two variables point to the same object.

.Equals() Method

Checks logical equality.

Can be overridden to compare object content.

Used when two objects represent the same data, even if stored in different memory locations.

Meaning:

.Equals() focuses on content, not memory.

Conceptual Summary

== → Physical Equality (same reference or same primitive value).

.Equals() → Logical Equality (same data/content).

In strings, both usually return true because string overrides equality behavior.
