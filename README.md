# Traffic-Congestion-Management-using-QUBO


## Problem Statement

This project focuses on managing traffic congestion during urban events by optimizing vehicle routes and traffic signal timings. The goals are to minimize total travel time, balance traffic loads, and prioritize emergency vehicles. The system dynamically adapts to real-time data to make optimal decisions. The problem is modeled as a **Quadratic Unconstrained Binary Optimization (QUBO)** problem, which is solved using a hybrid quantum-classical approach.

## Project Structure

### 1. [ReRouting Using QUBO](ReRouting_congestion_reduction.ipynb)
This notebook addresses vehicle routing optimization to reduce traffic congestion. 
Key steps include:
- Preprocessing map and GPS data.
- Identifying congestion points.
- Using Dijkstra’s and A* algorithms to generate alternative routes.
- Formulating a QUBO problem to optimize route assignments.
- Solving the QUBO with quantum annealing for optimized traffic flow.
Note: Currently, for simplicity, the input data has alternate routes written it, it can be improved to find other short alternative routes using Dijkstra’s or A* algorithms

### 2. [Traffic Signal Optimization Using QUBO](Traffic_Signal_Optimization.ipynb)
This notebook focuses on traffic signal control to minimize waiting times at intersections, particularly during high-demand events. The key steps include:
- Processing road and traffic density data.
- Formulating a QUBO matrix for signal control.
- Solving the QUBO problem using a quantum-classical hybrid solver.
- Dynamically updating traffic signal timings to optimize flow.
Note: Input data for city, roads and cars is randomly generated for simplicity purposes.

## Why QUBO?

Quantum annealers are designed to solve QUBO problems efficiently, as they are equivalent to the Ising model. QUBO formulation allows us to model complex traffic management tasks, including vehicle rerouting and signal control, for real-time optimization.

## Solution Workflow

### Traffic Congestion Optimization
1. Classical: Preprocess road network and traffic data.
2. Classical: Identify congested areas and generate alternative routes.
3. Classical: Formulate the QUBO problem for route assignments.
4. Quantum: Solve the QUBO using quantum annealing.
5. Classical: Redistribute cars based on optimized routes.
6. Iterate until congestion is minimized.

### Traffic Signal Optimization
1. Classical: Process map and traffic data.
2. Classical: Identify signals to synchronize and build a QUBO matrix.
3. Quantum: Optimize traffic flow by solving the QUBO problem.
4. Classical: Adjust signal timings based on the results.


## Conclusion

This project provides an efficient, scalable solution for optimizing traffic during urban events. The hybrid quantum-classical approach allows for real-time adjustments, making it effective for both vehicle routing and traffic signal control.
