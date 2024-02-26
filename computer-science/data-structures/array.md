---
description: Array data structure knowledge
cover: >-
  https://images.unsplash.com/photo-1622838805759-a64754fca2c6?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw2fHxhcnJheXxlbnwwfHx8fDE3MDg1MTY0Mjd8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Array

## What is an array ?

An array is an abstract data type, meaning its underlying implementation can change based on what programming language you use, however it follows a set of rules that are consistent through most programming languages.

This is a key idea to understand, as once you understand the fundamentals of what an array is, what operations it typically supports and when its used, are you able to implement it and use it effectively.

### Definition of an array

An array stores a collection of elements that have the same data type.

### Properties of an array

* Continuous block of memory
* Fixed size
* All elements have the same data type
* Each element is indexed

### Operations of an array

* Add an element to an array - O(N) time complexity
* Removing an element from an array - O(N) time complexity
* Accessing an element by index - O(1) time complexity&#x20;

| Operation | Time | Space |
| --------- | ---- | ----- |
| Access    | O(1) | O(1)  |
| Search    | O(N) | O(1)  |
| Insertion | O(N) | O(N)  |
| Deletion  | O(N) | O(N)  |

### Diagram of an array

<img src="../../.gitbook/assets/file.excalidraw (19).svg" alt="Visual representation of an array data structure" class="gitbook-drawing">

## Visual flow of operations

Here there will be a visual representation of what happens in most common operations for an array.

### Search for a element in an array

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (20).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (21).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (22).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (23).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 5" %}
<img src="../../.gitbook/assets/file.excalidraw (24).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Accessing a index from an array

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (16).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2 " %}
<img src="../../.gitbook/assets/file.excalidraw (17).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (18).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Insertion of a element into an array

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (25).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (26).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (27).svg" alt="" class="gitbook-drawing">


{% endtab %}
{% endtabs %}

## Code

{% code lineNumbers="true" fullWidth="false" %}
```csharp
// Here i create an array instaces of numbers with the size of 3
int[] numbers = new int[3];

// Here i assign the value at indx 0,1,2 the numbers 1,2,3
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;

// Here i loop through the array until i find the number 3 which returns true
bool doseNumberThreeExistsInArray = numbers.Contains(3);

// Re-assign the value at that index to be 4
numbers[2] = 4;

// Here i loop through the array until i find the number 3 which returns false
bool isThree = numbers.Contains(3);
```
{% endcode %}

## Variants

More topics worth knowing and understanding relating to arrays

### Multidimensional Arrays

A multidimensional array is an array that contains other arrays

#### 2D Arrays

A 2D array is an array of arrays, like a table with rows and columns

<figure><img src="../../.gitbook/assets/2D-array-representation.png" alt="Visual of 2D array"><figcaption><p>2D Array</p></figcaption></figure>

#### 3D Arrays

A 3D array is an array of 2D arrays

<figure><img src="../../.gitbook/assets/array3.png" alt="3D array"><figcaption><p>3D Array</p></figcaption></figure>

### Use cases

* Spatial grids like chess boards
* Image pixels (2D grid of color values)
* 3D volumetric data

### Code

{% code lineNumbers="true" %}
```csharp
// This is a 2D array
int[,] array2DDeclaration = new int[4, 2];

// This is a 3D array
int[,,] array3DDeclaration = new int[4, 2, 3];
```
{% endcode %}
