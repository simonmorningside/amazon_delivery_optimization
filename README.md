# Amazon Delivery Optimization

## Overview
This is a capstone project that is an optimization engine. This is supposed to minimize the cost of fulfillment per delivery and also try to improve delivery speed and on time delivery performance

## Business Problem
This problem matters because not only will it save Amazon money to have more optimized routes but customers will be happier when their items arrive on time more often

## Part 1: Optimization Engine (Complete ✓)

### What It Does
This optimization engine analyzes 150 possible combinations of delivery distance and warehouse load
to identify the Pareto frontier of efficient solutions that balance shipping cost 
vs delivery time.

### Key Findings
- ~3% of solutions are Pareto optimal
- ~145 dominated solutions were identified and should be avoided
- A single low-cost ground delivery option performs well across multiple strategies, while faster same-day options represent a high-cost, high-speed alternative on the frontier

### Running the Analysis
1. Ensure you have the required packages: `pandas`, `numpy`, `matplotlib`
2. Open `optimization_engine.ipynb`
3. Run all cells in order
4. Outputs will be saved to the `images/` folder

### Next Steps
Part 2 will add a constraint-aware decision agent that selects among these
Pareto optimal solutions based on business constraints and priorities.

## Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## Setup
Instructions coming soon...
