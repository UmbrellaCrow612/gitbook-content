---
description: Hash Tables data structure knowledge
cover: >-
  https://images.unsplash.com/photo-1579728866437-6397f3d89ec3?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw3fHxrZXlzfGVufDB8fHx8MTcwOTAyOTcyOXww&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Hash Tables

## What is a hash table

A Hash Table is an abstract data type, meaning its underlying implementation can change based on what programming language you use, however it follows a set of rules that are consistent through most programming languages.

This is a key idea to understand, as once you understand the fundamentals of what a Hash Table is, what operations it typically supports and when its used, are you able to implement it and use it effectively.

### Definition of a hash table

A key value pair container of data

### Properties of a hash table

* Each key must be unique&#x20;
* Multiple unique keys can have the same values
* Keys are hashed

### Operations of a hash table

* Adding keys / values- O(1) time complexity
* Removing a key / values -  O(1) time complexity
* Searching a key - O(1) time complexity

| Operation | Time | Space |
| --------- | ---- | ----- |
| Insert    | O(1) | O(N)  |
| Search    | O(1) | O(N)  |
| Delete    | O(1) | O(N)  |

### Diagram of a hash table

<img src="../../.gitbook/assets/file.excalidraw (43).svg" alt="Hash Table diagram" class="gitbook-drawing">

## Visual flow of operations

Here there will be a visual representation of what happens in most common operations for a hash table.

### Adding an item to a hash table

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (2).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (3).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 5" %}
<img src="../../.gitbook/assets/file.excalidraw (4).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Searching for an item in a hash table

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (5).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (6).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (7).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (8).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

### Removing an item from a hash table

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (9).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (10).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (11).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (12).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code

{% code lineNumbers="true" %}
```csharp
// Hash Table

// In c# we use a Dictionary as the hash table

// We create a number string key value pair 
Dictionary<int,string> numbersToWords = new Dictionary<int,string>();

// Adding key value pairs
numbersToWords[1] = "One";
numbersToWords[2] = "Two";
numbersToWords[3] = "Three";

// The hash table has key value pairs (1, "One"), (2, "Two"), (3, "Three")

// Searching for a given key

if(numbersToWords.ContainsKey(1)){
// It contains a key with value 1
}

// Compare a keys value

if(numbersToWords[1] == "One"){
// Then the value at key 1 is "One"
}

numbersToWords.Remove(1); // Removes key value pair

// The hash table has key value pairs (2, "Two"), (3, "Three")
```
{% endcode %}

## Variants

### Implamenation

Most other types have the same functionality as the base hash table however they differ under the hood, sometimes when you try to place an item in the table it collides with another after hashing, most alternatives try to solve this collision in other ways such as open addressing, multi mapping and more.

### Use cases

* Associative arrays/dictionaries
* Database indexing
* Caches
* Packet routing
