---
description: Depth First Search Knowledge
cover: >-
  https://images.unsplash.com/photo-1634117622592-114e3024ff27?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwzfHxncmFwaHxlbnwwfHx8fDE3MTA4NDY4ODF8MA&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Depth First Search

## **Depth-First Search (DFS)**

Depth-First Search (DFS) is an algorithm for traversing or searching a tree or graph data structure. It explores as far as possible along each branch before backtracking.

### Introduction to Depth-First Search

DFS is a recursive algorithm that uses the idea of exploring as far as possible along each branch before backtracking. It is used to traverse or search tree or graph data structures. DFS starts at the root node (or any arbitrary node of a graph) and explores as far as possible along each branch before backtracking.

### Explanation of Depth-First Search

The general steps for DFS are as follows:

1. Start at the root node (or any arbitrary node of a graph).
2. Push the root node to the stack and mark it as visited.
3. While the stack is not empty:
   * Pop the top node from the stack.
   * For each unvisited neighbor of the popped node:
     * Push the neighbor to the stack.
     * Mark the neighbor as visited.

### Time and Space Complexity of Depth-First Search

* **Time Complexity**: O(V + E), where V is the number of vertices and E is the number of edges in the graph.
* **Space Complexity**: O(V) in the worst case, when the graph is a linear data structure like a linked list or a stack.

### Visual Flow of Depth-First Search

```
         A
        / \
       B   C
      / \   \
     D   E   F
```

* **Step 1:**  Start at node A, mark it as visited, and push it to the stack.&#x20;

**Stack: \[A]**

* Step 2: Pop A from the stack. Push unvisited neighbors B and C to the stack.&#x20;

**Visited: \[A]** &#x20;

**Stack: \[C, B]**

* Step 3: Pop B from the stack. Push unvisited neighbors D and E to the stack.&#x20;

**Visited: \[A, B]**&#x20;

**Stack: \[E, D, C]**

* Step 4: Pop D from the stack (no unvisited neighbors).&#x20;

**Visited: \[A, B, D]**&#x20;

**Stack: \[E, C]**

* Step 5: Pop E from the stack (no unvisited neighbors).&#x20;

**Visited: \[A, B, D, E]**&#x20;

**Stack: \[C]**

* Step 6: Pop C from the stack. Push unvisited neighbor F to the stack.&#x20;

**Visited: \[A, B, D, E, C]**&#x20;

**Stack: \[F]**

* Step 7: Pop F from the stack (no unvisited neighbors).&#x20;

**Visited: \[A, B, D, E, C, F]**&#x20;

**Stack: \[]**

The DFS traversal order is: A, B, D, E, C, F.

<figure><img src="../../.gitbook/assets/Depth-First-Search.gif" alt=""><figcaption></figcaption></figure>

### Code Implementation of Depth-First Search

```csharp
using System;
using System.Collections.Generic;

public class Graph
{
    private int V; // Number of vertices
    private List<int>[] adj; // Adjacency list

    public Graph(int v)
    {
        V = v;
        adj = new List<int>[v];
        for (int i = 0; i < v; i++)
            adj[i] = new List<int>();
    }

    public void AddEdge(int v, int w)
    {
        adj[v].Add(w); // Add w to v's list
    }

    public void DFS(int s)
    {
        bool[] visited = new bool[V];
        Stack<int> stack = new Stack<int>();

        visited[s] = true;
        stack.Push(s);

        while (stack.Count != 0)
        {
            s = stack.Pop();
            Console.Write(s + " ");

            foreach (int i in adj[s])
            {
                if (!visited[i])
                {
                    visited[i] = true;
                    stack.Push(i);
                }
            }
        }
    }
}

public class Program
{
    public static void Main(string[] args)
    {
        Graph g = new Graph(6);

        g.AddEdge(0, 1);
        g.AddEdge(0, 2);
        g.AddEdge(1, 3);
        g.AddEdge(1, 4);
        g.AddEdge(2, 5);

        Console.WriteLine("Depth First Traversal (starting from vertex 0)");

        g.DFS(0);
    }
}
```

#### Output:

```
Copy codeDepth First Traversal (starting from vertex 0)
0 2 5 1 4 3
```

This implementation uses a `Graph` class to represent the graph as an adjacency list. The `AddEdge` method adds edges to the graph. The `DFS` method performs the Depth-First Search traversal starting from a given vertex `s`. It uses a boolean array `visited` to keep track of visited vertices and a stack to perform the traversal.

The `Main` method creates a sample graph and calls the `DFS` method starting from vertex 0. The output shows the Depth-First Traversal order of the vertices.

In this implementation, the graph is directed, and the vertices are represented by integers. You can modify the code to handle undirected graphs or use more descriptive names for the vertices, if needed.

### When to use Depth First Search

* **Graph Traversal**
* **Finding Connected Components**
* **Cycle Detection**
* **Topological Sorting**
* **Solving Mazes and Puzzles**
* **More**
