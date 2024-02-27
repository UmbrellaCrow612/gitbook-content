---
description: Hash Sets data structure knowledge
cover: >-
  https://images.unsplash.com/photo-1502570149819-b2260483d302?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxudW1iZXJ8ZW58MHx8fHwxNzA5MDM5NTU2fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Hash Sets

## What is a hash set

A Hash Set is an abstract data type, meaning its underlying implementation can change based on what programming language you use, however it follows a set of rules that are consistent through most programming languages.

This is a key idea to understand, as once you understand the fundamentals of what a Hash Set is, what operations it typically supports and when its used, are you able to implement it and use it effectively.

### Definition of a hash set

A container of data for unique data

### Properties of a hash set

* Each item is unique
* Items are not sorted in order
* Items are hashed for constant time lookup&#x20;

### Operations of a hash set

* Adding an item - O(1) time complexity
* Removing an item O(1) time complexity
* Searching for an item O(1) time complexity

| Operation | Time | Space |
| --------- | ---- | ----- |
| Insert    | O(1) | O(N)  |
| Remove    | O(1) | O(N)  |
| Search    | O(1) | O(N)  |

### Diagram of a hash set

<img src="../../.gitbook/assets/file.excalidraw (44).svg" alt="Diagram of a hash set" class="gitbook-drawing">
