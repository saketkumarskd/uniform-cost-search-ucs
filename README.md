# uniform-cost-search-ucs
Uniform Cost Search (UCS) assignment for pathfinding in weighted graphs — implemented in Python. Includes test cases, minimum-cost pathfinding, and a short write-up by Saket Kumar, IIT Patna).



---


# 🚀 Uniform Cost Search (UCS) — Pathfinding Assignment

## 🏞️ Project Overview
This project implements **Uniform Cost Search (UCS)** to find the **least-cost path** between cities in a weighted graph.  
Think of it as a simple **map navigation system**:

- **Nodes:** Cities  
- **Edges:** Roads connecting cities  
- **Weights:** Distance or travel cost  

The UCS algorithm guarantees the **shortest-cost path** from a start city to a destination, making it ideal for pathfinding problems.

---

## 🎯 Objectives
- Understand the **Uniform Cost Search (UCS)** algorithm.  
- Implement UCS in **Python** using a priority queue.  
- Solve real-world style **pathfinding problems**.  
- Analyze results and explain the algorithm’s behavior.

---

## 📊 Graph Representation
The graph used in this assignment:

```python
Graph = {
  'A': [('B', 2), ('C', 5)],
  'B': [('A', 2), ('C', 6), ('D', 1)],
  'C': [('A', 5), ('B', 6), ('D', 3), ('E', 8)],
  'D': [('B', 1), ('C', 3), ('E', 4)],
  'E': [('C', 8), ('D', 4)]
}
````

---

## 🧪 Test Cases

### Test Case 1 — Path from A → E

* **Start:** A
* **Goal:** E
* **Result:**

  * **Minimum Cost:** 7
  * **Path:** `['A', 'B', 'D', 'E']`

### Test Case 2 — Path from A → F (Extended Graph)

```python
'E': [('C', 8), ('D', 4), ('F', 2)],
'F': [('E', 2)]
```

* **Start:** A
* **Goal:** F
* **Result:**

  * **Minimum Cost:** 9
  * **Path:** `['A', 'B', 'D', 'E', 'F']`

---

## 📝 How UCS Works

1. UCS keeps track of the **total cost** to reach each city from the start.
2. Uses a **priority queue** to always expand the **cheapest path first**.
3. Continues until the **destination** is reached, ensuring **optimal path**.

---

## 💡 Insights

* UCS always finds the **optimal path** because it expands paths in **ascending order of cost**.
* If **all edge costs are equal**, UCS behaves like **Breadth-First Search (BFS)**.
* Works correctly **only with non-negative edge costs**.

---

## 🖥️ Usage Instructions

1. Open `UCS_Assignment_SaketKumar_2312res560.ipynb` in **Google Colab**.
2. Run cells step-by-step to see **paths and minimum costs**.
3. Or run `ucs_solution.py` locally with Python 3.

---

## 👨‍💻 Author

**Saket Kumar**
IIT Patna

---

## 🌟 Highlights

* Clear **graph representation**
* Step-by-step **UCS implementation**
* Fully **tested with multiple scenarios**
* Human-readable **explanations included**
* Works for **extended graphs and new cities**

---

## 📌 References

* Russell, S. & Norvig, P. (2010). *Artificial Intelligence: A Modern Approach*
* Python `heapq` documentation for priority queues

```
