# 🌳 Lowest Common Ancestor (Optimized Approach) – Binary Tree

## 📌 Overview

This project implements the **optimized approach to find the Lowest Common Ancestor (LCA)** in a **Binary Tree** using **recursion**.

Unlike the path-based approach, this method finds the LCA in a **single traversal**, making it more efficient and elegant.

This is one of the **most preferred approaches in technical interviews**.

---

# 🎯 Problem Statement

Given:

* The **root** of a binary tree
* Two nodes `n1` and `n2`

Find their **Lowest Common Ancestor (LCA)**.

---

# 🌿 Example

Binary Tree:

```id="tree_opt_lca"
        1
       / \
      2   3
     / \ / \
    4  5 6  7
```

If:

```id="nodes"
n1 = 4
n2 = 5
```

Then:

```id="result"
LCA = 2
```

---

# ⚙️ Optimized Approach (Single Traversal)

This approach avoids storing paths and instead uses **recursive backtracking**.

### Core Idea

* Traverse the tree once.
* If a node matches `n1` or `n2`, return that node.
* Recursively search in the left and right subtrees.
* Based on returned values, determine the LCA.

---

# 🔁 Algorithm Logic

At each node:

1️⃣ If the node is `null`, return `null`
2️⃣ If the node matches `n1` or `n2`, return the node
3️⃣ Recursively search in:

* Left subtree
* Right subtree

---

### Decision Making

After recursion:

* If **both left and right return non-null**
  → Current node is the **LCA**

* If only **one side returns non-null**
  → Return that side (LCA is deeper in the tree)

* If both return `null`
  → Return `null`

---

# 🔍 Visualization

```id="flow"
Check Root
   ↓
Search Left Subtree
Search Right Subtree
   ↓
If both sides return nodes → LCA found
Else return non-null side
```

---

# 🚀 Why This Approach is Better

### ✅ 1. Single Traversal

* Visits each node only once
* No need to store paths

---

### ✅ 2. Optimal Time Complexity

* Runs in **O(n)** time
* More efficient than the path-based approach in practice

---

### ✅ 3. No Extra Space for Paths

* Does not use additional lists or arrays
* Uses only recursion stack

---

### ✅ 4. Cleaner and Elegant Logic

* Simple recursive structure
* Easy to implement and explain in interviews

---

### ✅ 5. Industry Standard Approach

* This is the **expected solution in most coding interviews (Google, Amazon, etc.)**

---

# ⏱ Time and Space Complexity

| Complexity       | Value |
| ---------------- | ----- |
| Time Complexity  | O(n)  |
| Space Complexity | O(h)  |

Where:

* **n** = number of nodes
* **h** = height of the tree (recursion stack)

---

# 🧠 Concepts Used

* 🌳 Binary Trees
* 🔁 Recursion
* 🔍 Tree Traversal
* ⚡ Divide and Conquer
* 🔄 Backtracking

---

# 🎯 Learning Outcomes

After completing this problem you will understand:

✔ How to find LCA in a **single traversal**
✔ How recursion helps in solving tree problems efficiently
✔ Difference between **naive and optimized approaches**
✔ How to write clean and optimal tree algorithms

---

# 👨‍💻 Author

Developed as part of **Data Structures and Algorithms practice** 🚀
