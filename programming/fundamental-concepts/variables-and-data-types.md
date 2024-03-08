---
description: Fundamentals of Variables & Data Types
cover: >-
  https://images.unsplash.com/photo-1589630388147-68b3a2172e0c?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxidWNrZXR8ZW58MHx8fHwxNzA5OTE4MTIyfDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Variables & Data Types

## Variables

A variable is a named storage location in the computer's memory that can hold a value. It allows programmers to store and manipulate data during the execution of a program. In most programming languages, variables have the following characteristics:

1. `Name`: A variable is assigned a unique identifier, called its name. It should follow certain rules defined by the programming language, such as starting with a letter or underscore, containing alphanumeric characters, and avoiding reserved keywords.
2. `Value`: A variable can hold different types of data, such as numbers, text, or objects. The value can be assigned when the variable is created or modified during the program's execution.
3. `Type`: Variables have a specific data type that defines the kind of values they can hold and the operations that can be performed on them.
4. `Scope`: The scope of a variable determines where it can be accessed within a program. Variables can have local scope (limited to a specific block of code) or global scope (accessible throughout the entire program).

## Data Types

Data types specify the kind of data that can be stored in a variable. They determine the range of values that a variable can hold and the operations that can be performed on it. The choice of data type depends on the nature of the data being stored and the operations to be performed on that data. Common data types include:

#### **Numeric Types:**

* **Integers (int, long, short, byte):** Used for whole numbers without fractions. Think ages, counts, or quantities.
  * `int`: The standard choice for most whole-number needs.
  * `long`: For extremely large whole numbers.
  * `short`: Useful for memory conservation when you _know_ your numbers will be small.
  * `byte`: Represents whole numbers from 0 to 255; often used for colors or raw binary data.
* **Floating-Point (float, double, decimal):** Used to represent numbers with decimals. Accuracy and the range of values they can store differ between them.
  * `float`: Single-precision floating-point number. Common for many calculations.
  * `double`: Double-precision floating-point number. Offers greater precision than `float`, important for more complex or accuracy-dependent calculations.
  * `decimal`: Ideal for financial/monetary calculations where absolute precision is critical.

#### **Boolean Type (bool):**

* Represents logical values – `true` or `false`. Essential for decision-making (if-statements) and controlling the flow of your program.

#### **Character Types:**

* **Character (char):** Stores a single Unicode character like 'A', 'z', '3', or '@'. Enclosed in single quotes.
* **String (string):** A sequence of characters representing text. Examples: "Hello", "This is a sentence". Enclosed in double-quotes.

#### **Composite Types:**

* **Arrays:** Ordered collections of elements of the same type. You access elements using their index (position) in the array.
* **Lists:** Similar to arrays, but they can grow and shrink dynamically, making them more flexible in situations where the collection size may change.
* **Tuples:** Ordered collections that can store elements of different types. Useful when you need a quick group of related values together.
* **Dictionaries:** Store data in key-value pairs. Lookups are speedy since you access elements directly by their key.

#### **Custom Types:**

* **Classes:** Blueprints for creating objects. They define properties (data) and methods (actions on that data).
* **Structs:** Like classes but primarily used for holding data. Great for representing simple structures like points (x, y coordinates) or dates.

#### **Other Types:**

* C# offers additional data types. Always check the language references for details on these specialized types!

## Code Examples

{% code lineNumbers="true" %}
```csharp
// Numeric Types
int age = 30;
long largeNumber = 9223372036854775807;
short smallerNumber = 15000;
byte colorValue = 200;

float pi = 3.14159f;
double preciseValue = 1.23456789123456789;
decimal moneyAmount = 12345.67M;

// Boolean Type
bool isComplete = false;
bool isLoggedIn = true;

// Character Types
char initial = 'A';
char symbol = '#';

// String Type
string name = "Alice";
string message = "Welcome to C# data types!";

// Arrays
int[] numbers = { 1, 5, 10, 15 };
string[] colors = { "red", "green", "blue" };

// Custom Type (Struct)
struct Coordinates
{
    public int x;
    public int y;
}
Coordinates point = new()
{
    x = 5,
    y = 10
};

// Custom Type (Class)
class Person
{
    public string name;
    public int age;
    public bool isEmployed;
}
Person bob = new Person();
bob.name = "Bob";
bob.age = 25;
bob.isEmployed = true;
```
{% endcode %}
