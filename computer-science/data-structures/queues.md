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
