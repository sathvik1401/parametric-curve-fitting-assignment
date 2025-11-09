# **Objective**

This assignment aims to determine the unknown parameters **θ**, **M**, and **X** in the given parametric equations, with the goal of making the generated curve as close as possible to the provided \((x, y)\) data.

To quantify precision, the **L₁ loss** (mean absolute difference) between the observed data and the predicted values is minimized.

The parametric equations used are as follows:

$$
x = t \cos(\theta) - e^{M|t|} \sin(0.3t)\sin(\theta) + X
$$

$$
y = 42 + t \sin(\theta) + e^{M|t|} \sin(0.3t)\cos(\theta)
$$

---

# **Approach**

A **hybrid optimization approach** was adopted, consisting of two stages:

**1. Global Optimization (Differential Evolution)**
- Explores a large search space of possible values for **θ**, **M**, and **X**.  
- Helps locate a good starting point near the global minimum by avoiding local minima traps.

**2. Local Optimization (L-BFGS-B)**
- Refines the parameters found during the global search.  
- Improves accuracy and minimizes the **L₁ loss** to its lowest possible value.

---

### The combination of **global** and **local** optimization ensures:
- A more accurate fit to the data.  
- The closest possible match between predicted and observed points.

---

# **Results**

| **Parameter**        | **Symbol** | **Value**     |
|:---------------------:|:----------:|:--------------:|
| Theta (radians)       | θ          | 0.471929       |
| Theta (degrees)       | θ°         | 27.039529°     |
| M                     | M          | 0.023537       |
| X                     | X          | 54.527736      |
| Reduced L₁ Loss       | —          | 3515.287048    |

---

**Summary:**  
The hybrid approach (**Differential Evolution + L-BFGS-B**) successfully minimized the **L₁ loss**, providing an accurate parameter estimation for the given data.
