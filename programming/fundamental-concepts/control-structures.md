---
description: Fundamentals of Control Structures
cover: >-
  https://images.unsplash.com/photo-1624234594485-d7d329f6b515?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxjb250cm9sfGVufDB8fHx8MTcxMDA2NzQwM3ww&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Control Structures

## Introduction

Control structures in programming allow you to control the flow of execution based on certain conditions or perform repetitive tasks. They provide the ability to make decisions, perform actions selectively, and repeat code blocks.&#x20;

## Conditional Statements

Conditional statements allow you to make decisions in your code based on certain conditions. The most common type of conditional statement is the **if and else statement**, which evaluates a condition and executes a block of code if the condition is true.&#x20;

{% code lineNumbers="true" %}
```csharp
// Conditional Statements

int age = 17;

if(age > 18)
{
    Console.WriteLine("Over 18");
} else 
{
    Console.WriteLine("Below 18");
}
```
{% endcode %}

Additionally, you can use the **else if** clause to check multiple conditions sequentially.&#x20;

{% code lineNumbers="true" %}
```csharp
// Else if conditional statement

int age = 18;

if(age > 18)
{
    Console.WriteLine("Over 18");
} else if(age == 17)
{
    Console.WriteLine("Age is 17");
} else
{
    Console.WriteLine("Age is below 17");
}
```
{% endcode %}

### Loops

Loops are used to repeat a block of code multiple times until a certain condition is met.&#x20;

### For loop

Iterate a specific number of times when you know the number of repetitions beforehand.

{% code lineNumbers="true" %}
```csharp
// Example Code

for (initialization; condition; increment/decrement)
{
    // Code to be executed repeatedly
}

```
{% endcode %}

Print numbers from 1 to 10

{% code lineNumbers="true" %}
```csharp
// For loop

for (int i = 1; i <= 10; i++)
{
    Console.WriteLine(i);
}

```
{% endcode %}

### While Loop

Iterate as long as a condition remains true. Use when you don't know the exact number of iterations in advance.

{% code lineNumbers="true" %}
```csharp
// Example code

while (condition) 
{
    // Code to be executed repeatedly
}

```
{% endcode %}

Read user input until they enter "quit"

{% code lineNumbers="true" %}
```csharp
// While loop

string input = "";
while (input != "quit")
{
    Console.Write("Enter a word (or 'quit' to exit): ");
    input = Console.ReadLine();
}

```
{% endcode %}

### Do-While Loop

Similar to a `while` loop, but guarantees the code block executes at least once.

{% code lineNumbers="true" %}
```csharp
// Example Code

do
{
    // Code to be executed repeatedly
} while (condition); 

```
{% endcode %}

Get valid input from the user (ensuring they enter a number)

{% code lineNumbers="true" %}
```csharp
// do-while loop
int number;

do
{
    Console.Write("Enter a number: ");
} while (!int.TryParse(Console.ReadLine(), out number));

```
{% endcode %}

### Foreach loop

Iterate over every element in a collection (arrays, lists, etc.)

{% code lineNumbers="true" %}
```csharp
// Example code

foreach (var item in collection) 
{
    // Code to be executed for each item
}

```
{% endcode %}

Print the names in a list

{% code lineNumbers="true" %}
```csharp
// Foreach code

List<string> names = new List<string> { "Alice", "Bob", "Charlie" };
foreach (string name in names)
{
    Console.WriteLine(name);
}

```
{% endcode %}

### Important notes on control structures

* **Infinite Loops:** Be careful! If the conditions in your `while` or `do-while` loops never become false, you'll end up with an infinite loop that freezes your program.
* **`break` and `continue`:**
  * Use the `break` statement to exit a loop prematurely.
  * Use the `continue` statement to skip the rest of the current iteration and move to the next one.
