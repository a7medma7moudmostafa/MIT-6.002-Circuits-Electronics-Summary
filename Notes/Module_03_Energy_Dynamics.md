# Module 03: Energy & Dynamics 🔋⏳

In this module, we introduce time-dependent elements. We move beyond resistors to components that store energy, leading to circuits described by **Differential Equations**.

## 1. Energy Storage Elements
Unlike resistors that dissipate energy as heat, these elements store it:
* **Capacitor (C):** Stores energy in an **Electric Field**. ($i = C \frac{dv}{dt}$). It resists sudden changes in **Voltage**.
* **Inductor (L):** Stores energy in a **Magnetic Field**. ($v = L \frac{di}{dt}$). It resists sudden changes in **Current**.

## 2. First-Order Circuits (RC and RL)
When we have one energy storage element, the circuit is described by a first-order differential equation.
* **Transient Response:** The behavior of the circuit immediately after a switch changes (e.g., charging a capacitor).
* **Time Constant ($\tau$):** * For RC: $\tau = RC$
    * For RL: $\tau = \frac{L}{R}$
* **Key Insight:** After $5\tau$, the circuit practically reaches its **Steady State**.



## 3. Digital Circuit Dynamics (Power & Delay)
Why do our laptops get hot?
* **Propagation Delay:** It takes time to charge the gate capacitance of a MOSFET. This limits the maximum clock speed of a CPU.
* **Energy Consumption:** Every time a digital gate switches from `0` to `1`, energy ($\frac{1}{2}CV^2$) is stored and then dissipated as heat.
* **Power:** $P = f \cdot C \cdot V^2$ (This is why increasing frequency $f$ or voltage $V$ increases heat).

## 4. Second-Order Circuits (RLC)
With two energy storage elements (L and C), the system can **Oscillate**. The behavior depends on the **Damping Ratio**:
* **Overdamped:** Returns to equilibrium slowly without oscillating.
* **Underdamped:** Oscillates with decaying amplitude (Ringing).
* **Critically Damped:** The fastest way to reach equilibrium without oscillation.



## 5. State-Variable Analysis
A powerful, systematic way to solve complex dynamic circuits by focusing on the "State" of the system:
* **State Variables:** The voltage across capacitors ($v_C$) and the current through inductors ($i_L$).
* If you know the state at time $t$, and the inputs, you can predict the future state at $t + dt$.

---

### 💡 Ahmad’s Engineering Reflection:
This module explained the "Physics" of computing to me. It's fascinating to realize that the speed of my phone's processor is physically limited by how fast we can charge and discharge tiny capacitors (MOSFET gates). Also, seeing the math of a swinging pendulum appearing in an RLC circuit was a true "Aha!" moment—Engineering is truly universal.

