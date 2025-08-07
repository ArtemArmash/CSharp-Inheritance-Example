# C# Inheritance and Polymorphism Example (Auto Hierarchy)

This C# console application provides a clear and simple demonstration of Object-Oriented Programming (OOP) principles, specifically **inheritance** and **polymorphism**. It defines an abstract base class `Auto` and several derived classes (`Apperance`, `Salon`, `Tech`) that inherit from it.

## About The Project

This project was designed to illustrate how to build a class hierarchy in C#. An abstract class `Auto` acts as a blueprint, defining common properties and behaviors for any type of automobile characteristic. Concrete classes then inherit these traits and can provide their own specific implementations.

This example is a great way to understand:
*   **Abstract Classes**: How to create a base class that cannot be instantiated on its own but serves as a foundation for other classes.
*   **Inheritance**: How derived classes (`Apperance`, `Salon`, `Tech`) can reuse code from a base class (`Auto`).
*   **Polymorphism**: How a method (`Display`) can have different behaviors in different derived classes, demonstrated by the `override` keyword.
*   **Constructors in Inheritance**: How to call a base class constructor from a derived class constructor using the `base()` keyword.
*   **`protected` Access Modifier**: How to make members accessible to derived classes but not to the outside world.

## Project Structure

The code is contained within a single file and is composed of the following parts:

*   **`Auto` (Abstract Class)**:
    *   The base class for the hierarchy.
    *   Defines common `protected` fields like `Color`, `Number`, `Marka`, etc.
    *   Provides a constructor to initialize these common fields.
    *   Includes a `virtual` `Display()` method, which allows derived classes to override it.

*   **`Apperance`, `Salon`, and `Tech` (Derived Classes)**:
    *   These are concrete classes that inherit from `Auto`.
    *   Each has its own constructor that chains up to the `Auto` base constructor.
    *   Each **overrides** the `Display()` method to first print a unique header (e.g., "Apperance Details:") and then calls the base class's `Display()` method to print the common information.

*   **Main Program Logic**:
    *   The entry point of the script creates instances of each of the three derived classes (`Apperance`, `Salon`, `Tech`).
    *   It then calls the `Display()` method on each object, demonstrating how polymorphism works in practice.

## How to Run the Program

You will need the .NET SDK installed on your system to run this code.

1.  **Create a New Project**: Open a terminal or command prompt and create a new console application.
    ```sh
    dotnet new console -o AutoInheritanceDemo
    cd AutoInheritanceDemo
    ```
2.  **Copy the Code**: Copy the entire C# code from the source file.
3.  **Update `Program.cs`**: Open the `Program.cs` file that was created by `dotnet` and replace its contents with the code you copied.
4.  **Run the Application**: In your terminal, execute the following command:
    ```sh
    dotnet run
    ```

## Expected Output

When you run the program, you will see the details of each created object printed to the console, each with its own specific header, demonstrating the overridden `Display` method.

```
Apperance Details:
Color: Red
Number: 13123
Marka: BMW
Seats: 2
Quality: High
Maxspeed: 200 km/h
Avgspeed: 120 km/h
Salon Details:
Color: Green
Number: 41456
Marka: Audi
Seats: 1
Quality: Medium
Maxspeed: 185 km/h
Avgspeed: 100 km/h
Tech Details:
Color: Blue
Number: 53789
Marka: Mersedes
Seats: 7
Quality: Low
Maxspeed: 120 km/h
Avgspeed: 130 km/h
```
```
