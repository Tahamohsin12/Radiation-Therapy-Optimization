# 🏥 Radiation Therapy Optimization (Linear Programming)

### The Clinical Challenge
**The Problem:**
In cancer radiation therapy, doctors use external beams to destroy tumors. However, these beams also pass through and damage healthy anatomy and critical tissues nearby. The challenge is to find the "sweet spot" where the tumor is destroyed, but the patient remains safe.

**The Objective:**
Determine the precise intensity (dosage) for two radiation beams to ensure the **Tumor receives at least 6 kilorads** (to be effective) while keeping **Critical Tissues below 2.7 kilorads** (safety limit) and minimizing damage to the rest of the healthy anatomy.

---

### What I Did
1.  **Modeled the physics:** Built a mathematical model representing how radiation from two different angles is absorbed by different body parts (Tumor vs. Healthy Tissue).
2.  **Solved for patient safety:** Used Linear Programming to calculate the exact optimal dosage (**8.0 kRad from Beam 1, 3.0 kRad from Beam 2**) that meets all medical requirements.
3.  **Visualized the trade-offs:** Created a **Pareto Frontier** analysis to show doctors the "cost" of increasing tumor dosage in terms of healthy tissue damage, aiding in complex clinical decision-making.

---

### How It Works
* **Inputs:** Absorption coefficients for 3 body areas (Healthy, Critical, Tumor) across 2 beam sources.
* **Method:** Multi-objective Linear Programming using **Python** and **Gurobi Optimizer**.
* **Constraints:**
    * $\text{Tumor Dose} \ge 6.0 \text{ kRad}$ (Hard Constraint)
    * $\text{Critical Tissue Dose} \le 2.7 \text{ kRad}$ (Hard Constraint)
    * $\text{Minimize Healthy Tissue Dose}$ (Objective)

---

### 📉 Visual Output: The Pareto Frontier
<img width="612" height="468" alt="Pareto Froniter" src="https://github.com/user-attachments/assets/d5b2ccfd-4b97-48e4-a2a3-7fe6f2b6fd25" />

---

### Skills shown
Multi-objective linear programming · hard vs soft constraints · Pareto frontier for trade-off decisions · Python + Gurobi

### Why it matters in operations
Every operations decision trades one outcome against another: service level against cost, or throughput against quality. A Pareto frontier shows decision-makers exactly what each extra unit of one goal costs in the other, which is how I frame trade-offs for leadership.

### How to run
```bash
pip install gurobipy matplotlib jupyter
jupyter notebook Radiation_Therapy_Optimization.ipynb
```

*Context: developed from a group assignment in Managerial Decisions Modelling (UBC Sauder MBA, 2025).*
