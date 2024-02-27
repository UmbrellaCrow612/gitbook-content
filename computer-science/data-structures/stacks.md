---
description: Stacks data structure knowledge
cover: >-
  https://images.unsplash.com/photo-1532009877282-3340270e0529?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwzfHxzdGFja3xlbnwwfHx8fDE3MDg3MDM4Mjd8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Stacks

## What is a stack ?

A stack is an abstract data type, meaning its underlying implementation can change based on what programming language you use, however it follows a set of rules that are consistent through most programming languages.

This is a key idea to understand, as once you understand the fundamentals of what an stack is, what operations it typically supports and when its used, are you able to implement it and use it effectively.

### Definition of a stack

A Last In First Out container of data

### Properties of a stack

* Follows a stacking order of items
* Items that go last in are the ones to come out
* Push and pop off the stack
* Limited capacity - stack overflow

### Operations of a stack

* Add an item - O(1) time complexity
* Removing an item - O(1) time complexity
* Peeking an item - O(1) time complexity

| Operation | Time | Space |
| --------- | ---- | ----- |
| Push      | O(1) | O(N)  |
| Pop       | O(1) | O(1)  |
| Peek      | O(1) | O(1)  |

### Diagram of a stack

<img src="../../.gitbook/assets/file.excalidraw (2) (1) (1).svg" alt="" class="gitbook-drawing">

## Visual flow of operations

Here there will be a visual representation of what happens in most common operations for a stack.

### Adding an item to a stack

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (34).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (35).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (36).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (37).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Removing an item from a stack

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (38).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (39).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (40).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Peeking an item from a stack

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (9) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (1) (1) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (41).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code

{% code lineNumbers="true" %}
```csharp
// Stack code

// Creating a stack

Stack<int> numbers = new Stack<int>();

// Add numbers to it
numbers.Push(1);
numbers.Push(2);
numbers.Push(3);

// Current stack content in order - 3,2,1

// Remove an element
numbers.Pop();

// Current stack content in order - 2,1

numbers.Peek(); // returns 2

// Current stack content in order - 2,1

numbers.Pop(); // Remove 2
numbers.Pop();// Remove 1

// Stack is now empty

```
{% endcode %}

## Variants

More topics worth knowing and understanding relating to stacks

### Implementation details

There are stack variants but most come down to the underlying implementation being changed, this could be it uses arrays under the hood, linked lists or another data structure, these are used depending on the situation and which would offer better performance.

### Use cases

* Undo/redo operations in text editors
* Keeping track of function calls and call stack
* Browser back/forward button functionality
* Routing and pathfinding algorithms

