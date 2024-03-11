---
description: Fundamental knowledge of functions and methods
cover: >-
  https://images.unsplash.com/photo-1559249875-05d44554edd2?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxibG9ja3xlbnwwfHx8fDE3MTAxNTc0MDh8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Functions & Methods

## Introduction

Functions and methods are fundamental building blocks in programming, they enable you to organize your code into reusable units, just like little machines that perform specific tasks, which are essential building blocks of programming that allow you to break down complex tasks into smaller, reusable chunks of code, promoting code organization, modularity, and reusability.

## Functions

* **Self-contained Tasks:** A function is a block of code designed to perform a specific task.
* **Structure:**

```csharp
return_type function_name(parameters) {
    // Code to be executed
    return value; // Optional
}
```

### Example

```csharp
int calculateArea(int length, int width) {
    int area = length * width;
    return area;
}
```

## Methods

**Actions of Objects:** Methods are functions that are associated with objects in object-oriented programming . They define the behaviors or actions that an object can perform.

### Example

```csharp
string myString = "Hello World!";
int length = myString.Length();   // Method to get string length
string upperCase = myString.ToUpper(); // Method to convert to uppercase
```

## Calling functions and methods

**Using the Name:** To use a function or method, simply call it by name and provide any necessary arguments within parentheses.

### Example

```csharp
int rectArea = calculateArea(5, 10); // Calling the calculateArea function
Console.WriteLine("The area is: " + rectArea);
```

## **Function Parameters and Return Values**

* **Parameters:** Input values that you pass into a function or method.
* **Return Values:** A value that may be sent back from the function after it has executed its task.

### Example

```csharp
int findMaximum(int num1, int num2) {
    if (num1 > num2) {
        return num1;
    } else {
        return num2;
    }
}
```
