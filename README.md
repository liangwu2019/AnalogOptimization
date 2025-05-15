# Analog Optimization with Arbitrarily Small Execution-Time Certificate
This repository is for our submission "Arbitrarily Small Execution-Time Certificate: What was Missed in Analog Optimization". Analog Optimization, transforming optimization problems into ordinary differential equations (ODEs) and solving ODEs on analog computers, lacks theoretical foundations: (1) how to handle the infeasible issue, and (2) how to certify the equilibrium time for the transformed ODE.

We made up for the lack of theory in analog optimization: introducing (1) the Homogeneous Monotone Complementary Problem formulation (enabling infeasibility detection) and (2) the Newton-based fixed-time-stable scheme (making the equilibrium time $T_p$ of the transformed ODE can be prescribed by choosing the ODE's time coefficient as $k=\frac{\pi}{2T_p}$).

We consider a convex NLP $\min_{x\in\mathbb{R}^n}\quad f(x), s.t.\quad x\geq0, \quad g_i(x)\leq0, i=1,\cdots,m$, including linear programming (LP) and quadratic programming (QP). 

## Feasible cases
The LP_Infeasible.ipynb, QP_Infeasible.ipynb, and NLP_Infeasible.ipynb files are used to demonstrate the infeasibility detection capability, and the results show that the infeasibility detection rates for all cases are 100% (details are in the original manuscript).
![image](https://github.com/user-attachments/assets/2ca492fc-76fa-4017-be82-ee27698a0210)

## Infeasible cases
The LP_Feasible.ipynb, QP_Feasible.ipynb, and NLP_Feasible.ipynb files are used to demonstrate the infeasibility detection capability.
![image](https://github.com/user-attachments/assets/12369910-f83b-47b6-8d49-e23163102f85)

