# 🔌 Y-Bus Matrix Builder (MATLAB)

An interactive MATLAB program to construct the **Bus Admittance Matrix (Y-Bus)** for power system networks.

This tool allows users to input transmission line data in either **Impedance (R, X)** or **Admittance (G, B)** format and automatically generates the Y-Bus matrix with optional shunt admittances.

---

## 🚀 Features

- 🔄 **Dual Input Modes**
  - **Impedance Mode (R, X)** → Automatically converts to admittance
  - **Admittance Mode (G + jB)** → Direct input

- 🧮 **Automatic Y-Bus Formation**
  - Correct off-diagonal updates
  - Proper diagonal accumulation
  - Line charging susceptance handled (B/2 model)
  - Self-loop support

- ✏️ **Interactive Editing**
  - Review and modify branch data before matrix generation

- ⚡ **Optional Bus Shunt Admittances**
  - Add shunt elements directly to diagonal entries

- 📊 **Formatted Complex Output**
  - Displays Y-Bus matrix in standard complex form

---

## 🧠 Mathematical Background

For a transmission line:

Z = R + jX  

Admittance:

Y = 1 / Z = (R - jX) / (R² + X²)

### Y-Bus Formation Rules

- Off-diagonal elements:

  Yᵢⱼ = -Y_line

- Diagonal elements:

  Yᵢᵢ = Sum of connected admittances + Shunt admittance

- Line charging susceptance is divided equally:

  B/2 added to each connected bus

---

## 📂 Program Workflow

1. Enter number of buses
2. Enter number of branches
3. Select input mode (Impedance / Admittance)
4. Enter branch data
5. Review and edit entries (optional)
6. Add shunt admittances (optional)
7. Generate and display final Y-Bus matrix

---

The program converts impedances into admittances and constructs the complete Y-Bus matrix.

---

## 🎓 Applications

- Power Flow (Load Flow) Analysis
- Fault Analysis
- Power System Studies
- Academic Laboratory Experiments
- Teaching & Research Simulations

---

## 📌 Requirements

- MATLAB (R2016b or later recommended)
- No additional toolboxes required

---

## 📈 Why Use This Tool?

✔ Reduces manual calculation errors  
✔ Saves time for large systems  
✔ Easy to modify and extend  
✔ Ideal for students and researchers  

---

## 👨‍💻 Author

Developed for academic and power system analysis purposes.

---

## 📜 License

This project is open-source and free to use for educational purposes.
