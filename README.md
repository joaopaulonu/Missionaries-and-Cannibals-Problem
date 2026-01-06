# 🛶 Logic & Algorithms: Missionaries and Cannibals Problem

![Language](https://img.shields.io/badge/Language-Java%20%2F%20Pseudocode-blue)
![Category](https://img.shields.io/badge/Category-Computational%20Thinking-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Concept](https://img.shields.io/badge/Concept-State%20Space%20Search-lightgrey)

---

## 🌟 Overview

This repository contains the study and resolution of the **Missionaries and Cannibals Challenge**, a classic fundamental problem used to teach programming logic and Artificial Intelligence.

The focus here is the practical application of the four pillars of **Computational Thinking**:
1. **Decomposition**: Breaking down the crossing into small, manageable movements.
2. **Pattern Recognition**: Identifying back-and-forth cycles.
3. **Abstraction**: Focusing on essential data (number of people and boat position).
4. **Algorithms**: Creating the exact sequence of steps for the solution.

---

## 🧩 The Challenge

The **Missionaries and Cannibals** is a classic river-crossing puzzle that requires logic and strategic planning. 

### The Objective
Move **three missionaries (M)** and **three cannibals (C)** from one river bank to the other using a boat that can carry a **maximum of two people**.

### Constraints & Rules
* **Characters**: 3 Missionaries and 3 Cannibals.
* **Boat Capacity**: The boat can hold at most 2 people and cannot move by itself (it requires at least one person to operate).
* **Safety Rule**: On either bank, if there are missionaries present, the number of cannibals **cannot exceed** the number of missionaries. If they do, the missionaries will be "eaten."
* **Goal**: Successfully transport all 6 characters from the starting bank to the destination bank.

---

## 📌 Algorithm Analysis (State-Space Representation)

Below is the state representation used to ensure that safety constraints are never violated.  
**Critical Rule:** Cannibals (C) $\le$ Missionaries (M) on both banks (whenever $M > 0$).

| Step | Left Bank | Boat Action | Right Bank | Logical Explanation |
| :--- | :--- | :--- | :--- | :--- |
| **0** | **3M, 3C** | (Start) | 0M, 0C | Initial State. |
| **1** | 3M, 1C | 2C $\rightarrow$ | 0M, 2C | Two cannibals cross. |
| **2** | 3M, 2C | $\leftarrow$ 1C | 0M, 1C | One cannibal returns to pilot. |
| **3** | 3M, 0C | 2C $\rightarrow$ | 0M, 3C | Remaining cannibals cross. |
| **4** | 3M, 1C | $\leftarrow$ 1C | 0M, 2C | One cannibal returns. |
| **5** | 1M, 1C | 2M $\rightarrow$ | 2M, 2C | **The Switch**: Missionaries move forward. |
| **6** | 2M, 2C | $\leftarrow$ 1M, 1C | 1M, 1C | Mixed return to maintain balance. |
| **7** | 0M, 2C | 2M $\rightarrow$ | 3M, 1C | All missionaries on the Right Bank. |
| **8** | 0M, 3C | $\leftarrow$ 1C | 3M, 0C | One cannibal returns for the others. |
| **9** | 0M, 1C | 2C $\rightarrow$ | 3M, 2C | Two more cannibals cross. |
| **10** | 0M, 2C | $\leftarrow$ 1C | 3M, 1C | Final return. |
| **11** | **0M, 0C** | 2C $\rightarrow$ | **3M, 3C** | **Goal Reached.** |

---

## 🎯 Key Technical Skills

| Category | Topics Covered |
| :--- | :--- |
| **Modeling** | State-space representation, constraint management. |
| **Logic** | Problem decomposition, validation rules (if/else logic). |
| **Algorithms** | Sequential execution, search strategies. |
| **Programming** | Object-oriented concepts (Bank, Boat) and state transitions. |

---

## 🛠️ Technology & Tools

| Detail | Value |
| :--- | :--- |
| **Concept** | Computational Thinking |
| **Logic Foundation** | Alura - Java Programming Course |
| **Documentation** | Markdown / GitHub |

---

## 🚀 How to Run

Since this is an algorithmic logic project:
1. Analyze the step-by-step flow in the table above.
2. Check the `algoritmo.txt` file (or similar) for the natural language description.
3. For code implementations, refer to the `/src` folder.

---

## 📬 Contact Me
<div align="center"> 
  <a href="https://www.linkedin.com/in/nunes-andrade" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="https://instagram.com/jp_nunes.andrade" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white"></a>
  <a href="mailto:jpnunesandrade26@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://www.alura.com.br/indica-dev/jpnunesandrade26" target="_blank"><img src="https://img.shields.io/badge/Alura-0077B5?style=for-the-badge&logo=alura&logoColor=white"></a> 
</div>
