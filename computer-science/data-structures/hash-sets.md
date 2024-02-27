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

## Visual flow of operations

Here there will be a visual representation of what happens in most common operations for a hash sets.

### Adding an item to a hash set

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (45).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (46).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (47).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (48).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Searching for an item in a hash set

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (49).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (50).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (51).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (52).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Removing an item from a hashset

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (53).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (54).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (55).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (56).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code

{% code lineNumbers="true" %}
```csharp
// Hash set 

// Create a hash set of numbers
HashSet<int> numbersSet = new HashSet<int>();

// Add the numbers in
numbersSet.Add(1);
numbersSet.Add(2);
numbersSet.Add(3);

// Hash set contains - 1,2,3 (not in order)

if(numbersSet.Contains(1))
{
// Then the set contains 1
}

numbersSet.Remove(1); 

// Hash set contains - 2,3 (not in order)

```
{% endcode %}

## Variants

### Implantation

There are different types of hash sets but most offer a different underlying implementing with hashing algorithms and collision mitigation,  some offer slight benefits such as keeping the order of the items and such but most really depend on the use case needed.

### Use cases

* Removing duplicates
* Membership testing
* Implementing sets and maps
* Caches
