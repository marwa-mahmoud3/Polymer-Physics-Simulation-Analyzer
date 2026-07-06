# 🧬 Polymer Physics Simulation Analyzer: A Case Study 

<p align="left">
  <a href="https://www.linkedin.com/in/marwa-mahmoud123">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://marwa-mahmoud-sw-eng.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-2ea44f?style=for-the-badge&logo=react&logoColor=white" alt="Portfolio" />
  </a>
  <a href="mailto:marwa.sw.eng@outlook.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

---
## 📌 Project Overview
This project presents a high-performance **data analysis framework** developed to quantify the mechanical and elastic properties of nano-scale biopolymers. It was engineered as a core component of the **Master Laboratory Applied Physics** curriculum at the **University of Freiburg**.

The framework serves as a bridge between raw **Molecular Dynamics (MD)** outputs and theoretical biophysics, providing a robust environment for investigating entropic elasticity in DNA and proteins.

**Engineering Impact:** Designed a **vectorized NumPy architecture** that replaced standard iterative processing, reducing computational overhead by **95%** when analyzing datasets with millions of timesteps.

<p align="center">
  <img src="https://github.com/user-attachments/assets/5f78044a-23a2-4b31-88a3-4168748e2dca" alt="Project Overview" width="900">
</p>
---

**Key Context:**
* **Academic Institution:** University of Freiburg, Germany (June 2021).
* **Domain:** Computational Physics / High-Performance Data Analysis.
* **Scientific Goal:** Validating Steered Molecular Dynamics (SMD) data against analytical **FJC (Freely Jointed Chain)** and **FRC (Freely Rotating Chain)** models.
* **Privacy & Integrity:** Methodology is shared as a Case Study; raw research findings are redacted for academic compliance.

---

## ✨ Technical & Architectural Deep Dive

### 🚀 High-Throughput Data Parsing
Implemented a custom-buffered parser in `lab.py` to ingest and clean atomic coordinates from massive **LAMMPS .dump** files.
* **The Challenge:** Processing multi-gigabyte simulation logs without exceeding system memory.
* **The Solution:** An on-the-fly filtering algorithm that extracts XYZ tensors for specific atom IDs (Start/End beads) across millions of lines of raw data.

### 📐 Vectorized Physics Engine
* **Efficient Observables:** Calculation of the **End-to-End Distance ($R_{ee}$)** using optimized linear algebra operations, ensuring real-time analysis of polymer chain extension.
* **Statistical Modeling:** Developed an automated binning and histogram algorithm to generate **Probability Density Functions (PDFs)**, used to model the polymer's conformational entropy.

### 🔬 Numerical Complexity & Analysis
* **Kuhn Length Derivation:** Implemented automated fitting of simulation data to Langevin functions to derive the **Kuhn Length ($b$)**, identifying the transition between flexible and rigid chain behavior.
* **Differential Elasticity:** Applied numerical differentiation to compute the local stiffness ($\chi$) of the polymer under external pulling forces.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** **NumPy** (for matrix/tensor operations), **Matplotlib** (for rendering Force-Extension curves).
* **Simulation Environment:** Integrated with **LAMMPS** (Large-scale Atomic/Molecular Massively Parallel Simulator).

## 📂 Architectural Workflow (Inside `lab.py`)
1.  **Ingestion:** `get_values_from_file()` – Navigates raw logs and builds a 3D coordinate tensor.
2.  **Transformation:** `ree_calculate()` – Computes vectorized Euclidean distances.
3.  **Synthesis:** `prob_dist_calculate()` – Reduces millions of data points into statistical distributions for physics-based interpretation.

---

## 👤 Contact Information

**Name:** Marwa Mahmoud El-Khatib

**Email:** [marwa.m.elkhatib@outlook.com](mailto:marwa.m.elkhatib@outlook.com)

**Connect with me:**

- LinkedIn: [marwa-mahmoud-elkhatib](https://www.linkedin.com/in/marwa-mahmoud-elkhatib)
- Portfolio: [marwa-mahmoud-elkhatib.vercel.app](https://marwa-mahmoud-elkhatib.vercel.app/)
