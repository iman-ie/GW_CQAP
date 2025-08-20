# GW_CQAP
Gromov-Wasserstein Optimization Methods Comparison
This repository contains implementations and comparisons of various optimization methods for solving the Gromov-Wasserstein (GW) problem, formulated as a Capacitated Quadratic Assignment Problem (CQAP).
Overview:
The code compares multiple approaches for solving optimal transport problems:

GW Default: Standard Gromov-Wasserstein with default initialization

GW MultiInit: GW with multiple random initializations

EGW: Entropic Gromov-Wasserstein with various epsilon values

FGW: Fused Gromov-Wasserstein with different alpha parameters

GA: Genetic Algorithm approach

Exact: Global optimal solution using Gurobi (for small instances)

# Requirements

numpy

scipy

gurobipy

pot (Python Optimal Transport)

Installation

pip install numpy scipy pot
# For Gurobi (requires license):
pip install gurobipy
Usage
pythonpython main.py
The script will:

Generate a random problem instance (agents and tasks with positions and capacities)
Run all optimization methods
Compare computational times and objective values
Display results and performance gaps

Key Features
Problem Generation

Random agent/task positions in 2D space
Variable capacities and demands with mass balance
Euclidean distance matrices for cost computation

Optimization Methods
GW MultiInit Algorithm:

Tries multiple random valid initializations
Uses Sinkhorn projections to ensure constraint satisfaction
Selects best solution across all trials

Genetic Algorithm:

Custom implementation with tournament selection
Blend crossover and adaptive mutation
Constraint projection using Sinkhorn iterations

Exact Solution:

Gurobi-based quadratic programming formulation
Global optimality guarantee for small problems
Branch-and-bound with non-convex settings

Results
The code outputs:

Objective values for each method
Computational times
Performance gaps relative to best solution
Best performing method identification
