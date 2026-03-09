# ⚡ Interactive Y-Bus Builder (MATLAB)

## 📌 Overview
This project implements an **Interactive Y-Bus Matrix Builder** in **MATLAB** for power system network analysis.

The program allows users to **construct the Bus Admittance Matrix (Y-Bus)** by entering transmission line data interactively. It supports multiple input formats including **impedance (R, X)** and **admittance (G, B)** and automatically converts values when required.

The script also allows users to:
- Review and edit branch data before computation
- Include line charging susceptance
- Add optional shunt admittances at buses

The **Y-Bus matrix** is widely used in **load flow analysis, fault analysis, and power system stability studies**.

---

## 🚀 Features

✔ Interactive MATLAB interface for building Y-Bus  
✔ Supports **two input modes**:
- Impedance mode (R, X)
- Admittance mode (G, B)

✔ Automatic conversion from **impedance to admittance**  
✔ Supports **full and short data formats**  
✔ Allows **editing branch inputs before final calculation**  
✔ Supports **optional shunt admittances at buses**  
✔ Displays the **final Y-Bus matrix clearly formatted**

---

## ⚙️ Input Modes

The program provides two modes for entering line parameters.

### 1️⃣ Impedance Mode
Users provide **resistance and reactance**, and the program converts them to admittance.

#### Full Format
```
[from_bus  to_bus  R  X  B_total]
```

Example:
```
[1 2 0.02 0.4 0.1]
```

#### Short Format
```
[from_bus  to_bus  X]
```

Example:
```
[1 2 0.4]
```

Assumptions:
- R = 0
- B_total = 0

---

### 2️⃣ Admittance Mode
Users directly enter the **admittance values**.

#### Full Format
```
[from_bus  to_bus  G  B_series  B_total]
```

Example:
```
[1 2 0.5 -2.0 0.1]
```

#### Short Format
```
[from_bus  to_bus  G]
```

Example:
```
[1 2 0.5]
```

Assumptions:
- B_series = 0
- B_total = 0

---

## 📥 Program Inputs

The program will ask for the following inputs:

### Number of Buses
```
Enter number of buses
```

### Number of Branches
```
Enter number of branches (lines)
```

### Input Mode
```
1 → Impedance Mode
2 → Admittance Mode
```

### Branch Data
Each branch is entered as a MATLAB vector:

Example:
```
[1 2 0.02 0.4 0.1]
```

Where:

| Parameter | Description |
|----------|-------------|
| from_bus | Starting bus |
| to_bus | Ending bus |
| R | Resistance |
| X | Reactance |
| B_total | Line charging susceptance |

---

## ✏️ Editing Branch Inputs

After entering all branches, the program shows a **summary of the branch data**.

Users can:
- Review entered values
- Edit any branch
- Re-enter data before building the Y-Bus matrix

---

## ➕ Optional Shunt Admittances

Users may add shunt admittances to buses.

Format:
```
[bus  G  B]
```

Example:
```
[3 0.0 0.25]
```

Where:

| Parameter | Description |
|----------|-------------|
| bus | Bus number |
| G | Conductance |
| B | Susceptance |

---

## 📊 Example Output

The program prints the **final Y-Bus matrix** in complex form.

Example:

```
FINAL Y-BUS MATRIX

  0.50000 + j-2.50000    -0.50000 + j2.00000
 -0.50000 + j2.00000      0.50000 + j-2.50000
```

---

## 📂 Repository Structure

```
ybus-interactive-builder
│
├── ybus_interactive.m
└── README.md
```

---

## 🎯 Applications

🔹 Power system load flow analysis  
🔹 Network modeling  
🔹 Fault analysis studies  
🔹 Electrical power system simulation  
🔹 Engineering education and research

---

## 🛠️ Technologies Used

- MATLAB
- Power System Analysis
- Matrix Computation

---

## 👨‍💻 Author

**Likith Kumar**

Electrical and Electronics Engineering  
CHRIST (Deemed to be University)
