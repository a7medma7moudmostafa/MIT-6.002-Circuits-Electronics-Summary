# Module 02: Electronic Devices 🔌

In this module, we break the "Linearity" barrier. We introduce devices that don't follow Ohm's Law in a straight line, specifically the **MOSFET**, and learn how to use them to build both Digital and Analog systems.

## 1. Non-linear Circuit Analysis
Most real-world devices (Diodes, Transistors) are non-linear. To analyze them, we used two main methods:
* **Analytical Solution:** Solving non-linear equations (usually hard and involves exponentials).
* **Graphical Analysis:** Finding the **Operating Point (Q-point)** by intersecting the device characteristic curve with the **Load Line**.

## 2. The Digital Abstraction
This is where Computer Science meets Electrical Engineering. We define:
* **Voltage Thresholds:** Using $V_L$ and $V_H$ to represent `0` and `1`.
* **The Static Discipline:** A guarantee that if inputs satisfy valid logic levels, the circuit will produce valid logic levels at the output. This allows us to chain thousands of gates together without signal degradation.

## 3. The MOSFET as a Switch (S Model)
The **MOSFET** (Metal-Oxide-Semiconductor Field-Effect Transistor) is the building block of modern processors. 
* **Switch Model:**
    * If $V_{GS} < V_T$: The switch is **Open** (Off).
    * If $V_{GS} \ge V_T$: The switch is **Closed** (On).
* This model is used to build **CMOS Inverters** and logic gates (AND, OR, NAND).



## 4. Small-Signal Analysis (The Magic of Amplification)
How do we turn a non-linear device into a linear amplifier? 
1. **Bias the device:** Set a DC operating point (Q-point) in the saturation region.
2. **Inject a Small Signal:** Add a tiny AC signal ($v_{gs}$) on top of the DC bias.
3. **Linearization:** If the signal is small enough, the curve looks like a straight line.
* **Result:** We get a **Voltage Gain** ($G = \frac{v_{out}}{v_{in}}$).

## 5. MOSFET Models for Analysis
* **S Model:** Simple switch (for digital).
* **SR Model:** Switch with an internal resistance $R_{ON}$ (to calculate power and delay).
* **SCS Model:** Switched Current Source (for saturation/amplification analysis).

---

### 💡 Ahmad’s Engineering Reflection:
This module was a game-changer for me. Understanding the **Digital Abstraction** made me realize how we can build reliable computers out of "noisy" and "imperfect" analog components. Also, the transition from seeing a MOSFET as a simple switch to seeing it as a **Voltage-Controlled Current Source** is the foundation of all the electronics we use today.
