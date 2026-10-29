**CPFxDRL-SuperFast Airfoil Optimizer**



**Overview:**

This repository contains the source code for the CPFxDRL-SuperFast Airfoil Optimizer. It integrates the Constructive Piecewise Functions (CPF) shape parameterization method with Deep Reinforcement Learning (DRL) algorithms to perform aerodynamic shape optimization. The environment is built on top of 'Gymnasium' and uses the Proximal Policy Optimization (PPO) algorithm from 'Stable\_Baselines3' (It can be switched to other algorithms available at 'Stable\_Baselines3' library), coupled with NeuralFoil for ultra-fast, vectorized aerodynamic evaluations (The solver can be switched to other solvers by some changes in '\_run\_solver' def).



**Prerequisites:**

To run this code, you need to have the following python packages installed:

* gymnasium
* stable\_baselines3
* numpy
* neuralfoil



**External Software:**

Unlike the baseline version of CPFxDRL, this SuperFast version uses NeuralFoil (a Python-based Physics-Informed Neural Network, PINN) instead of XFOIL for flow-field solving. Therefore, no external software installation is required beyond the Python packages.



**Setup \& Configuration:**

Before running the code, be sure about locating the 'USER SETTINGS' section to set your directories/CPU cores, and adjust CPF variables according to your own airfoil (Current code is adjusted for NACA 0012 airfoil).



**Outputs:**

* Hall of Fame: During training phase, any geometry that breaks the current record is saved in the 'Hall\_of\_Fame' directory.
* Trained Model: The final trained DRL (PPO) model is saved in your working directory.
* Results File: A summary report containing the aerodynamic performance (Final L/D, Cd, Cm\_abs\_max, delta\_Cm), computational costs and the optimized CPF variables is written to 'results.txt' inside the logs directory.



**License:**

This project is open-source and distributed under the MIT License. You are free to use, modify, and distribute this software for academic and commercial purposes, provided that proper credit and citation are given to the original author.

