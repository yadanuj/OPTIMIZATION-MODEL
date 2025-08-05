# OPTIMIZATION-MODEL
*COMPANY*: CODTECH IT SOLUTIONS

 *NAME*: ANUJ YADAV

*INTERN ID*: CT04DH1868

*DOMAIN*: DATA SCIENCE

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTHOSH

# 📊 Linear Programming Optimization using PuLP - Task 4

---

## 📈 Project Overview

This repository demonstrates a practical application of **Linear Programming (LP)** to solve real-world **optimization problems** using Python. The project utilizes the **PuLP library**, a powerful tool for modeling and solving linear optimization problems efficiently.

Through this task, I explored how to define and solve an LP problem involving **maximizing or minimizing an objective function** subject to **constraints**. Linear Programming is widely used in domains like supply chain management, finance, operations research, and resource allocation.

---

## 🎯 Objective

- To design and solve a **Linear Programming problem** using Python.
- Learn how to **model constraints, decision variables, and objective functions** in code.
- Optimize a given objective function under real-world constraints.
- Use **PuLP** for easy formulation and solving of LP problems.

---

## 🧰 Technologies Used

| Tool/Library     | Purpose                                     |
|------------------|---------------------------------------------|
| Python 3.x       | Core programming language                   |
| PuLP             | LP modeling and optimization solver         |
| Jupyter Notebook | Interactive coding and result visualization |
| Matplotlib       | Optional for result visualization           |
| NumPy (optional) | Numerical computation                       |

---

## 📊 Problem Description

The project addresses a sample **resource allocation problem** where the goal is to **maximize profit or minimize cost** given certain resource constraints.

### Example Scenario:
- Suppose a factory produces two products **A** and **B**.
- Each product requires specific amounts of resources (e.g., time, labor, material).
- The company wants to **maximize total profit** while ensuring resource usage stays within available limits.

---

## 🧩 Workflow Breakdown

### 1️⃣ Define Decision Variables
- `x` = number of units of Product A to produce
- `y` = number of units of Product B to produce

### 2️⃣ Objective Function
- Maximize profit = `Profit_A * x + Profit_B * y`

### 3️⃣ Constraints
- Resource constraints: time, labor, materials, etc.
- For example:
  - `Resource1_A * x + Resource1_B * y <= Available_Resource1`
  - `Resource2_A * x + Resource2_B * y <= Available_Resource2`
- Additional constraints like non-negativity: `x >= 0, y >= 0`

---

## 💻 Sample Code Snippet

```python
import pulp

# Initialize the problem
model = pulp.LpProblem("Maximize_Profit", pulp.LpMaximize)

# Decision variables
x = pulp.LpVariable('x', lowBound=0, cat='Continuous')
y = pulp.LpVariable('y', lowBound=0, cat='Continuous')

# Objective function
model += 40 * x + 30 * y, "Total Profit"

# Constraints
model += 2 * x + y <= 100  # Resource 1
model += x + 2 * y <= 80   # Resource 2

# Solve
model.solve()
print(f"Optimal x = {x.varValue}")
print(f"Optimal y = {y.varValue}")
print(f"Max Profit = {pulp.value(model.objective)}")
```

---

## 📂 Project Structure

```
.
├── Task_4_Linear_Programming_Optimization.ipynb  # Main notebook
├── README.md                                     # Project documentation
└── requirements.txt                              # (Optional) Dependencies list
```

---

## 📊 Results & Insights

- The LP solver computes the **optimal values of decision variables** `x` and `y`.
- The **maximum profit** (or minimized cost) is also calculated.
- The results can be extended to more complex problems with multiple variables and constraints.

---

## 🔍 Applications

- **Business Strategy**: Optimize profit, cost, or output.
- **Logistics**: Route optimization, resource allocation.
- **Finance**: Portfolio optimization.
- **Manufacturing**: Product mix optimization under limited resources.

---

## 🚀 How to Run

1. Clone the repo:
```bash
git clone https://github.com/yourusername/linear-programming-task.git
cd linear-programming-task
```

2. Install PuLP:
```bash
pip install pulp
```

3. Open the Jupyter Notebook:
```bash
jupyter notebook Task_4_Linear_Programming_Optimization.ipynb
```

4. Run all cells to execute and view the optimization result.

---

## 📊 Future Enhancements

- Add **visualization of constraint regions and optimal point**.
- Solve more complex **integer or mixed-integer programming** problems.
- Integrate with **real-world datasets** for business use cases.
- Add **automated input form** for custom constraints/objectives.

---

#Output:

<img width="1919" height="751" alt="Image" src="https://github.com/user-attachments/assets/014463c9-03d0-44ef-827e-cd8fccf7efd8" />
