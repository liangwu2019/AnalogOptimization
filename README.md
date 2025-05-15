# AnalogOptimization
This repository is for our submission "Arbitrarily Small Execution-Time Certificate: What was Missed in Analog Optimization". Analog Optimization, transforming optimization problems into ordinary differential equations (ODEs) and solving ODEs on analog computers, lacks theoretical foundations: (1) how to handle the infeasible issue, and (2) how to certify the equilibrium time for the transformed ODE.

We made up for the lack of theory in analog optimization: introducing (1) the Homogeneous Monotone Complementary Problem formulation and (2) the Newton-based fixed-time-stable scheme (making the equilibrium time $T_p$ of the transformed ODE can be prescribed by choosing the ODE's time coefficient as $k=\frac{\pi}{2T_p}$).

![image](https://github.com/user-attachments/assets/6c352cf8-8d5f-4f6b-b63d-3d6c0bc3cf97)
