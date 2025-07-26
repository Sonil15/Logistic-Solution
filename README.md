# Vehicle Routing Problem (VRP) Solver Using Genetic Algorithm

This repository provides an advanced implementation of the Vehicle Routing Problem (VRP), leveraging a Genetic Algorithm (GA) to optimize delivery routes for a fleet of vehicles operating from a central depot. The solution focuses on minimizing total distance traveled and balancing the workload across all vehicles.

<img width="580" height="455" alt="image" src="https://github.com/user-attachments/assets/1671d47e-e773-48ad-b554-a78967b76f81" />

## Features

- **Multiple Vehicle Support:** Flexible configuration of the number of vehicles serving randomized delivery locations.
- **Randomized Delivery Points Generator:** Automated generation of delivery locations for simulation purposes.
- **Genetic Algorithm Framework (DEAP):**  
  - **Chromosome Representation:** Encodes complete routes for all vehicles.  
  - **Selection:** Tournament selection preserves high-quality solutions.  
  - **Crossover:** Ordered Crossover (OX) ensures feasible offspring routes.  
  - **Mutation:** Swap mutation promotes exploration and avoids local optima.  
- **Multi-Objective Fitness:** Optimizes for both total distance minimization and balanced distribution of deliveries.  
- **Visualization Tools:** Dynamic plotting of vehicle routes and performance progression via `matplotlib`.

### Empirical Results (default parameters):

-Vehicles: 10
-Delivery points: 100
-After 300 generations, total route distance is reduced from ~28,000 to under 13,500 units.
-Load balancing (standard deviation of route lengths) typically drops below 300 units.
(Refer to notebook console output for precise statistics per run.)



## Repository Overview

- **Data Generation Module:** Scripts to generate and manage randomized delivery locations.  
- **VRP Core Logic:** Implements chromosome encoding, fitness evaluation, and genetic operators tailored to VRP.  
- **Visualization Module:** Functions to graphically present the best solutions across generations.  
- **Jupyter Notebook:** `vehicle_Routing_Algorithm.ipynb` integrates all components for interactive exploration and experimentation.

## Installation

Ensure Python 3.x is installed, then run:

```
pip install matplotlib deap
```

## Usage Instructions

1. Launch the Jupyter Notebook:  
   `vehicle_Routing_Algorithm.ipynb`
2. Configure parameters before execution:  
   - `num_vehicles`: Number of delivery vehicles.  
   - `num_locations`: Number of delivery points.  
   - Genetic Algorithm parameters: `population_size`, `generations`, `cxpb` (crossover probability), `mutpb` (mutation probability).  
3. Run notebook cells sequentially to execute the GA.  
   - Monitor console outputs for best fitness progress.  
   - View evolving route visualizations updating in real-time.

## Output

- Console logs provide generation-by-generation feedback on the best solutions.  
- Graphical plots illustrate vehicle routes, facilitating visual assessment of route optimization quality.

## Applications

This VRP solver serves as both a benchmark for logistics optimization and an educational tool for studying evolutionary algorithms in practical scenarios. Adaptations and tuning may be required for specific operational environments or enterprise deployment.

**Author:** Developed for research and practical exploration of Genetic Algorithms in solving complex routing problems.

*This README is adapted for your project from a reference implementation for clarity and professionalism.*
