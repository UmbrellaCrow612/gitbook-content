---
description: Binary Search algorithm knowledge
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

Time - **Olog(N)**

Space - **O(1)**

## Visual flow of binary search

## Code implementation of binary search

## When to use a binary search
