Objective

This assignment aims at determining the unknown parameters θ, M and X in the given parametric equations with the view of making the generated curve as close to the given (x, y) data as possible.

To quantify precision, the L1 loss (mean absolute difference) between the error data and the prediction values is minimized.


**LaTeX Format**
```
\left(
t\cos(0.471929)
 - e^{0.023537|t|}\sin(0.3t)\sin(0.471929)
 + 54.527736,
\ 42 + t\sin(0.471929)
 + e^{0.023537|t|}\sin(0.3t)\cos(0.471929)
\right)
```




Approach

To address this issue, a hybrid optimization approach was adopted that amalgamates to two stages:

1.Global Optimization (Differential Evolution):
	The algorithm examines a large amount of possible θ, M, and X.
	It assists in obtaining a good starting point near the global minimum by the evasion of the local traps.

2.Local Optimization (L-BFGS-B):
	The L-BFGS-B optimisation method is used to refine the parameters once a region near-optimal is found by the global search.
	This step makes the process more accurate and minimizes the L 1 loss at its minimal possible value.


The global and local approach is the most successful in terms of delivering an accurate fit for the data and providing the most accurate match possible between the predicted and observed points.

Results


| Parameter | Symbol | Value |
|------------|:--:|:--:|
| Theta (radians) | θ | 0.471929 |
| Theta (degrees) | θ° | 27.039529° |
| M | M | 0.023537 |
| X | X | 54.527736 |
| Reduced L₁ Loss | — | 3515.287048 |

