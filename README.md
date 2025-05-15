# Analog Optimization with Arbitrarily Small Execution-Time Certificate
This repository is for our submission "Arbitrarily Small Execution-Time Certificate: What was Missed in Analog Optimization". Analog Optimization, transforming optimization problems into ordinary differential equations (ODEs) and solving ODEs on analog computers, lacks theoretical foundations: (1) how to handle the infeasible issue, and (2) how to certify the equilibrium time for the transformed ODE.

We made up for the lack of theory in analog optimization: introducing (1) the Homogeneous Monotone Complementary Problem formulation (enabling infeasibility detection) and (2) the Newton-based fixed-time-stable scheme (making the equilibrium time $T_p$ of the transformed ODE can be prescribed by choosing the ODE's time coefficient as $k=\frac{\pi}{2T_p}$).

We consider a convex NLP $\min_{x\in\mathbb{R}^n}\quad f(x), s.t.\quad x\geq0, \quad g_i(x)\leq0, i=1,\cdots,m$, including linear programming (LP) and quadratic programming (QP). 

## Feasible cases
The LP_Infeasible.ipynb, QP_Infeasible.ipynb, and NLP_Infeasible.ipynb files are used to demonstrate the infeasibility detection capability. First, 100 feasible LPs, QPs, convex NLPs are generated. Then to make these LPs, QPs, and convex NLPs infeasible, we add the contradictory constraint: $\sum_{i=1}^nx_i\leq-1$, namely $A\leftarrow[A;-\mathbf{1}_n^\top],b\leftarrow[b;1]$. The equilibrium time is prescribed as $T_p=1$ seconds. By retrieving the values of $\tau,\kappa$ at $t=1$ seconds, all examples in three LP, QP, and convex NLP cases show that $\kappa>\tau$ and $\tau\rightarrow0$, which indicates that the infeasibility detection rates for all cases are $\mathbf{100\%}$. The trajectory of $\tau$ and $\kappa$ for a representative case is plotted in the following:
![image](https://github.com/user-attachments/assets/2ca492fc-76fa-4017-be82-ee27698a0210)

## Infeasible cases
The LP_Feasible.ipynb, QP_Feasible.ipynb, and NLP_Feasible.ipynb files are used to demonstrate the correctness of our derived equation: $k=\frac{\pi}{2T_p}$. Experiment (1): choosing different prescribed equilibrium time $T_p=1$, $0.8$, $0.6$, $0.4$, $0.2$, $0.1$; Experiment (2): choosing various initial conditions, $z^0=5e,z^0=10e,z^0=2e,z^0=40e, z^0=60e,z^0=80e$, under the same  prescribed equilibrium time $T_p=1$. The results for LP, QP, and convex NLP are plotted in the following, respectively, which validates that the equilibrium time of our proposed ODE can be prescribed arbitrarily small and independent of the initial condition.
![image](https://github.com/user-attachments/assets/12369910-f83b-47b6-8d49-e23163102f85)

