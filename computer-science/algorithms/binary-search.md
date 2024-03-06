---
description: Binary Search algorithm knowledge
cover: >-
  https://images.unsplash.com/photo-1586769852836-bc069f19e1b6?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw0fHxzZWFyY2h8ZW58MHx8fHwxNzA5NzI1ODU4fDA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Binary Search

## Introduction to binary search ?

Searches through a sorted list of items, halving the list of items each time it, until it finds the target item and returns its index.

## Explanation of a binary search

Steps:

1. Initialise a left pointer to start at the beginning of the array and a right pointer at the end
2. While the left pointer hasn't reached the right pointer we search through the array
3. Calculate the midpoint index by adding the left and right pointer and dividing by 2
4. Get the value at the midpoint index and compare it to the target value
5. If the value at the midpoint is greater than our target, we want to search the lower half of the array
6. If the value at the midpoint is less than our target, we want to search the upper half of the array
7. Continue to do this until either the left and right pointer reach each other, find our targets index or we don't and return -1 or the index of where it should have been

### Time and space complexity of a binary search

Time - Olog(N)

Space - O(1)

## Visual flow of binary search

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (65).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (67).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (68).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (69).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code implementation of binary search

{% code lineNumbers="true" %}
```csharp
// Binary Search

int BinarySearch(int[] sortedNumbers, int targetValue)
{
    // We start the left pointer at the beginning
    int leftPointer = 0;
    // We start the right pointer at the end
    int rightPointer = sortedNumbers.Length - 1;

    // while the pointers havent reached each other
    while (leftPointer <= rightPointer)
    {
        // Calculate the index of the midpoint
        int midPoint = (leftPointer + rightPointer) / 2;
        // Get the value at that index
        int valueAtTheMidPoint = sortedNumbers[midPoint];

        // Compare if the value is our target
        if (valueAtTheMidPoint == targetValue)
        {
            // if it is we return the index of the target value
            return midPoint;

            // If the target is greater than the value
        }
        else if (valueAtTheMidPoint < targetValue)
        {
            // Search the top right half
            leftPointer = midPoint + 1;
        }
        else
        {
            // Search the bottom left half
            rightPointer = midPoint - 1;
        }

    }

    // If we did not find the value we return -1 or the leftPointer which would
    // be its index if it was in the array
    return -1;
}
```
{% endcode %}

## When to use a binary search

* When you have sorted array of items
* When you need to find a value in Olog(N) time
