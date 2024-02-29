---
description: Queues data structure knowledge
cover: >-
  https://images.unsplash.com/photo-1584614207146-a64524f5806a?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwyfHxxdWV1ZXxlbnwwfHx8fDE3MDg5Njc1ODB8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Queues

## What is a queue ?

A queue is an abstract data type, meaning its underlying implementation can change based on what programming language you use, however it follows a set of rules that are consistent through most programming languages.

This is a key idea to understand, as once you understand the fundamentals of what an queue is, what operations it typically supports and when its used, are you able to implement it and use it effectively.

### Definition of a queue

A First In First Out container of data

### Properties of a queue

* Follows the convention of a real life queue
* First in first out
* Join the queue (Enqueue)
* Leave the queue (Dequeue)

### Operations of a queue

* Enqueue an item - O(1) time complexity
* Dequeue an item - O(1) time complexity
* Peek the first item - O(1) time complexity

| Operation        | Time | Space |
| ---------------- | ---- | ----- |
| Enqueue (Insert) | O(1) | O(1)  |
| Dequeue (Delete) | O(1) | O(1)  |
| Peek (Access)    | O(1) | O(1)  |

### Diagram of a queue

<img src="../../.gitbook/assets/file.excalidraw (42).svg" alt="Diagram of a queue data structure" class="gitbook-drawing">

## Visual flow of operations

Here there will be a visual representation of what happens in most common operations for a queue.

### Adding an item to a queue

Also know as Enqueuing

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (13).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (1) (1) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (2) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (3) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 5" %}
<img src="../../.gitbook/assets/file.excalidraw (4) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Deleting an item from a queue

Also known as Dequeuing

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (5) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (6) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Peeking an item from a queue

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (7) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (8) (1) (1).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code

{% code lineNumbers="true" %}
```csharp
// Queue code

// Start with an empty queue
Queue<int> numbersQueue = new Queue<int>();

// Adding item to the queue
numbersQueue.Enqueue(1);
numbersQueue.Enqueue(2);
numbersQueue.Enqueue(3);

// Queue numbers - 1,2,3

numbersQueue.Peek(); // returns 1

numbersQueue.Dequeue(); // return 1 and also removes it from the queue

// Queue numbers - 2,3

numbersQueue.Dequeue(); // return 2 and also removes it from the queue
numbersQueue.Dequeue(); // return 3 and also removes it from the queue

// Queue is empty
```
{% endcode %}

## Variants

More topics worth knowing and understanding relating to queues

### Priority Queue

A regular queue but with priority on each element, meaning if one item has a higher priority than another then it will be the first to come out.&#x20;

<figure><img src="../../.gitbook/assets/Priority-Queue-min-1024x512.png" alt=""><figcaption><p>Priority Queue Visual</p></figcaption></figure>

### Use cases

* Job/task scheduling
* Messaging
* Load balancing
* Emergency room
