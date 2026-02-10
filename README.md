# Heaps & Shortest Path Performance Analysis

**Binary Heap vs Fibonacci Heap vs Hollow Heap in Dynamic Shortest Path Problems**

##  Overview

This project is a comparative case study that evaluates the performance of three advanced heap data structures — **Binary Heap**, **Fibonacci Heap**, and **Hollow Heap** — when used as priority queues within **Dijkstra’s shortest path algorithm**.

All heap structures are implemented from scratch and integrated into a generic Dijkstra framework. The system measures runtime efficiency, heap operations performance, and structural properties under dynamic routing conditions.

The project also includes large-scale performance testing using graph datasets of different sizes and densities.

---

##  Learning Objectives

* Implement Binary Heap, Fibonacci Heap, and Hollow Heap from scratch.
* Compare theoretical vs empirical performance.
* Integrate heaps into Dijkstra’s algorithm using a generic priority queue interface.
* Evaluate:

  * insert
  * extract-min
  * decrease-key operations
* Record heap structural properties:

  * height
  * number of trees
  * consolidation behavior
* Generate analytical insights and performance comparisons.

---

##  Case Study Background

A smart logistics company manages automated delivery routing where traffic conditions change in real-time. Edge weights frequently update, requiring repeated shortest-path recomputation.

Since Dijkstra’s algorithm relies heavily on priority queue operations (especially decrease-key), selecting the optimal heap structure significantly affects performance, memory usage, and scalability.

This project simulates that environment to determine the most efficient heap structure.

---

## Project Tasks

1. Implement Binary Heap, Fibonacci Heap, and Hollow Heap.
2. Integrate each heap with Dijkstra’s shortest path algorithm.
3. Run experiments on multiple graph datasets.
4. Record:

   * operation execution time
   * heap structural statistics
5. Compare results and produce analytical insights.

---

##  Implementation Requirements

### Heap Operations

Each heap must support:

* `insert(key, value)`
* `find_min()`
* `extract_min()`
* `decrease_key(node, new_key)`
* `delete(node)` *(optional for Binary Heap)*

### Integration

* Implement Dijkstra’s algorithm using a **generic PriorityQueue interface**.
* Swap heap implementations without changing algorithm logic.

---

##  Performance Measurement

### Execution Metrics

Measure:

* Total runtime of Dijkstra per heap
* Average operation time:

  * insert
  * extract_min
  * decrease_key

### Structural Metrics

For Fibonacci and Hollow heaps record:

* Heap height
* Number of trees in root list
* Number of cascading cuts (Fibonacci)

---



##  Sample Experiments

### Experiment A — Static Routing

* Run Dijkstra once per graph using all three heaps.
* Record total runtime.

### Experiment B — Operation Profiling

* Generate ~100,000 random priority queue operations.
* Measure time per operation.

---

##  Example Output (Sample)

| Heap      | Nodes | Edges  | Insert (μs) | Extract-Min (μs) | Decrease-Key (μs) | Total Runtime (s) | Height | #Trees | Memory |
| --------- | ----- | ------ | ----------- | ---------------- | ----------------- | ----------------- | ------ | ------ | ------ |
| Binary    | 10000 | 190900 | 1.2         | 3.1              | 4.0               | 0.002             | 100    | –      | –      |
| Fibonacci | 10000 | 190900 | 1.0         | 2.1              | 0.9               | 0.001             | 19     | 10     | 10 MB  |
| Hollow    | 10000 | 190900 | 1.3         | 2.5              | 0.8               | 0.0015            | 12     | 659    | 7 MB   |

---

## Code Requirements

* Three graph datasets are provided.
* Program must:

  1. Prompt user to select a dataset file.
  2. Load and process graph data.
  3. Run Dijkstra using each heap.
  4. Display performance table.
  5. Generate a `.txt` file containing the same output.

---

##  Deliverables

* Source code for:

  * Binary Heap
  * Fibonacci Heap
  * Hollow Heap
* Dijkstra integration module
* Test suite:

  * correctness tests
  * performance tests
* Performance report:

  * tables
  * plots
* Final analytical comparison across graph sizes and heaps.

---

##  Report Outline

### 1. Theoretical Overview

* Binary Heap
* Fibonacci Heap
* Hollow Heap

### 2. Implementation Details

* Data structures
* Priority queue interface
* Algorithm integration

### 3. Experimental Setup

* Dataset description
* Hardware/software environment

### 4. Results & Analysis

* Operation timing comparison
* Heap structure statistics
* Trade-off discussion

### 5. Conclusion & Recommendations

---

##  Bonus Challenges

* Implement **parallel Dijkstra** (multi-source or multi-threaded).
* Compare heap scalability under parallel workloads.
* Add visualization of: 

  * heap height evolution
  * root list changes during execution.

---

##  Technologies Suggested

* C / C++ / Java / Python
* STL restricted (for heap logic)
* CSV/Text graph datasets
* Matplotlib / Excel for visualization

---

##  License

This project is for academic and research purposes.
# Heap-and-shortest-path-Algo-project-
