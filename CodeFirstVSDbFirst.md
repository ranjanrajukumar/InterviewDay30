# Code First & Database First Approach (EF Core)
🔹 Q1. What is the Code First Approach?

The Code First approach means we start by writing C# model classes first.
Entity Framework Core then uses these classes to automatically create the database using migrations.

This approach is best when:

The project is new

Developers want full control over database design

The database structure changes frequently

🔹 Q2. How does the Code First Approach work?

Create model classes in C#.

Create a DbContext class.

Run Add-Migration to generate migration files.

Run Update-Database to create or update the database.

EF Core reads the model classes and builds the database tables automatically.

🔹 Q3. What is the Database First Approach?

In the Database First approach, the database is created first using SQL.
After the database exists, EF Core scaffolds the model classes and DbContext from the database.

This approach is useful when:

The database already exists

DBAs manage the database schema

There are many stored procedures and triggers

🔹 Q4. How does the Database First Approach work?

Create the database manually in SQL Server.

Install EF Core packages in your project.

Run the Scaffold command:

Scaffold-DbContext "connection-string" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models


EF Core generates model classes and a DbContext based on your tables.

🔹 Q5. What is the difference between Code First and Database First?
Code First	Database First
Start with C# classes	Start with database tables
EF Core creates the database	EF Core generates classes from DB
Good for new projects	Good for existing databases
Easy to use migrations	Schema handled by DBA
🔹 Q6. When should you use Code First?

Use Code First when:

You are building a new application

You want to generate database from C# classes

You plan to modify the schema frequently

You prefer domain-driven design

🔹 Q7. When should you use Database First?

Use Database First when:

The database already exists

The organization uses DBA-managed schemas

The schema is complex

Stored procedures and views are widely used

🔹 Q8. What is Migration in EF Core?

Migration is a feature that helps you create and update the database schema without losing data.

Common commands:

Add-Migration
Update-Database
Remove-Migration


Migrations track changes made to the model classes.

🔹 Q9. Can we switch between Code First and Database First?

Yes, you can switch:

To Database First, use scaffolding to generate models from the database.

To Code First, write classes manually and use migrations.

However, syncing both approaches requires careful management to avoid conflicts.

🔹 Q10. Which approach is better?

It depends on the project:

Code First → Best for new, flexible applications

Database First → Best when the database already exists or DBAs control the schema
