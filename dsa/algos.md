Here’s a detailed list of commonly used algorithms, categorized by their problem-solving domains, along with their time complexities:

### **1. Sorting Algorithms:**

| **Algorithm**       | **Best Case**    | **Average Case**  | **Worst Case**     | **Space Complexity** | **Usage**                                         |
|---------------------|------------------|-------------------|--------------------|----------------------|--------------------------------------------------|
| **Bubble Sort**      | O(n)             | O(n^2)            | O(n^2)             | O(1)                 | Simple but inefficient for large data sets.     |
| **Selection Sort**   | O(n^2)           | O(n^2)            | O(n^2)             | O(1)                 | Simple, inefficient for large datasets.         |
| **Insertion Sort**   | O(n)             | O(n^2)            | O(n^2)             | O(1)                 | Efficient for small datasets or nearly sorted.  |
| **Merge Sort**       | O(n log n)       | O(n log n)        | O(n log n)         | O(n)                 | Stable, good for large datasets.                |
| **Quick Sort**       | O(n log n)       | O(n log n)        | O(n^2)             | O(log n)             | Fast, but O(n^2) worst case.                    |
| **Heap Sort**        | O(n log n)       | O(n log n)        | O(n log n)         | O(1)                 | Used in priority queues.                        |

---

### **2. Searching Algorithms:**

| **Algorithm**        | **Best Case**    | **Average Case**  | **Worst Case**     | **Space Complexity** | **Usage**                                             |
|----------------------|------------------|-------------------|--------------------|----------------------|------------------------------------------------------|
| **Linear Search**     | O(1)             | O(n)              | O(n)               | O(1)                 | Simple, unsorted data.                               |
| **Binary Search**     | O(1)             | O(log n)          | O(log n)           | O(1)                 | Sorted arrays or lists.                              |
| **Hash Search**       | O(1)             | O(1)              | O(n)               | O(n)                 | Hash tables for fast lookups.                        |
| **Exponential Search**| O(log n)         | O(log n)          | O(log n)           | O(1)                 | Suitable for unbounded or exponentially growing lists. |

---

### **3. Graph Algorithms:**

| **Algorithm**              | **Time Complexity**  | **Space Complexity** | **Usage**                                     |
|----------------------------|----------------------|----------------------|----------------------------------------------|
| **Breadth-First Search (BFS)** | O(V + E)            | O(V + E)             | Shortest path in unweighted graphs, level-order traversal. |
| **Depth-First Search (DFS)**  | O(V + E)            | O(V + E)             | Traversing graphs, topological sorting.     |
| **Dijkstra's Algorithm**     | O(E + V log V)       | O(V + E)             | Shortest path in weighted graphs (non-negative weights). |
| **Bellman-Ford Algorithm**   | O(VE)                | O(V)                  | Shortest path in graphs with negative weights. |
| **Floyd-Warshall Algorithm** | O(V^3)               | O(V^2)               | All-pairs shortest path.                    |
| **Prim's Algorithm**         | O(E + V log V)       | O(V + E)             | Minimum spanning tree (MST).                 |
| **Kruskal's Algorithm**      | O(E log E)           | O(E + V)             | Minimum spanning tree (MST).                 |

---

### **4. Dynamic Programming Algorithms:**

| **Algorithm**                 | **Time Complexity**  | **Space Complexity** | **Usage**                                         |
|-------------------------------|----------------------|----------------------|--------------------------------------------------|
| **Knapsack Problem**           | O(nW)               | O(nW)                | Solving optimization problems with bounded weights. |
| **Longest Common Subsequence (LCS)** | O(mn)             | O(mn)                | Finding longest common subsequence.              |
| **Fibonacci Sequence**         | O(n)                | O(n)                 | Computing Fibonacci numbers efficiently.          |
| **Longest Increasing Subsequence (LIS)** | O(n^2)         | O(n)                 | Finding LIS in a sequence.                       |

---

### **5. Divide and Conquer Algorithms:**

| **Algorithm**                 | **Time Complexity**  | **Space Complexity** | **Usage**                                     |
|-------------------------------|----------------------|----------------------|----------------------------------------------|
| **Merge Sort**                 | O(n log n)          | O(n)                 | Sorting large datasets.                      |
| **Quick Sort**                 | O(n log n)          | O(log n)             | Sorting (average case).                      |
| **Binary Search**              | O(log n)            | O(1)                 | Searching in sorted arrays.                  |

---

### **6. Greedy Algorithms:**

| **Algorithm**                 | **Time Complexity**  | **Space Complexity** | **Usage**                                      |
|-------------------------------|----------------------|----------------------|-----------------------------------------------|
| **Kruskal’s Algorithm**        | O(E log E)           | O(E + V)             | Minimum Spanning Tree (MST).                  |
| **Prim’s Algorithm**           | O(E + V log V)       | O(E + V)             | Minimum Spanning Tree (MST).                  |
| **Huffman Coding**             | O(n log n)           | O(n)                 | Data compression algorithms.                  |

---


### **7. Miscellaneous Algorithms:**

| **Algorithm**                 | **Time Complexity**  | **Space Complexity** | **Usage**                                          |
|-------------------------------|----------------------|----------------------|---------------------------------------------------|
| **Euclidean Algorithm (GCD)**  | O(log(min(a, b)))    | O(1)                 | Finding the greatest common divisor (GCD) of two numbers. |
| **Sieve of Eratosthenes**      | O(n log log n)       | O(n)                 | Finding all primes less than n.                   |
| **Topological Sort**           | O(V + E)             | O(V + E)             | Sorting vertices in a directed acyclic graph (DAG). |
| **Ford-Fulkerson Algorithm**   | O(VE^2)              | O(VE)                | Maximum flow in a flow network.                   |

---

### **Choosing the Best Algorithm:**
- **For Sorting:** Merge Sort, Quick Sort, or Heap Sort based on data size and constraints.
- **For Searching:** Use Binary Search for sorted data, or Hash Maps for efficient lookups.
- **For Graph Problems:** Dijkstra’s or Bellman-Ford for shortest path, DFS/BFS for traversal.
- **For Dynamic Programming:** Knapsack, LCS for optimization problems.
- **For Greedy Problems:** Kruskal’s or Prim’s for MST, Huffman for data compression.

Understanding the problem, analyzing its requirements, and comparing the time complexities of the algorithms will help you select the best algorithm for the given task.