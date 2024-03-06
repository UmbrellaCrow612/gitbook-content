---
description: Bubble Sort Sorting algorithm knowledge
cover: >-
  https://images.unsplash.com/photo-1521192520982-5d6ca468a30f?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwyfHxzb3J0fGVufDB8fHx8MTcwOTczMjA0NHww&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Bubble Sort

## Introduction to Bubble Sort ?

Sorts a list of comparable items in either ascending or descending order&#x20;

## Explanation of a Bubble Sort

Steps:

1. Start at the first value
2. Go through each item and compare it to the next item in the sequence&#x20;
3. If the next item is bigger than the current item swap them
4. Repeat the above until all items are sorted

### Time and space complexity of a Bubble Sort

$$
Time = O(N)^2
$$

$$
Space= O(N)
$$

## Visual flow of Bubble Sort

{% tabs %}
{% tab title="Step 1" %}
<img src="../../.gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 2" %}
<img src="../../.gitbook/assets/file.excalidraw (2).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 3" %}
<img src="../../.gitbook/assets/file.excalidraw (3).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 4" %}
<img src="../../.gitbook/assets/file.excalidraw (4).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 5" %}
<img src="../../.gitbook/assets/file.excalidraw (5).svg" alt="" class="gitbook-drawing">
{% endtab %}

{% tab title="Step 6" %}
<img src="../../.gitbook/assets/file.excalidraw (6).svg" alt="" class="gitbook-drawing">
{% endtab %}
{% endtabs %}

## Code implementation of Bubble Sort

{% code lineNumbers="true" %}
```csharp
// Bubble Sort

public int[] BubbleSort(int[] numbers)
{
    int temp;
    for (int i = 0; i < numbers.Length - 1; i++)
    {
        for (int j = 0; j < numbers.Length - i - 1; j++)
        {
            if (numbers[j] > numbers[j + 1])
            {
                temp = numbers[j];
                numbers[j] = numbers[j + 1];
                numbers[j + 1] = temp;
            }
        }
    }
    return numbers;
}
```
{% endcode %}

## When to use a Bubble Sort

* Dont need to really use it in the real world or in a interview
* If you need to sort something in a question or real world use built in methods for sorting

