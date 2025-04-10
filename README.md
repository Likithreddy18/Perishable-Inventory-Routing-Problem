# Perishable Inventory Routing Problem

## Overview
This repository contains the implementation and analysis of a multi-objective optimization approach to the Perishable Inventory Routing Problem (PIRP). The project compares two methodologies:
1. A deterministic Co-Solver approach
2. The NSGA-II genetic algorithm

PIRP integrates inventory management and vehicle routing decisions under perishability constraints, to optimize three key objectives:
- Maximizing profit
- Improving service levels
- Reducing greenhouse gas emissions

## Problem Context
Managing perishable products presents significant challenges across various industries, including:
- Food industry
- Agri-food sector
- Pharmaceuticals
- Blood transfusion centers

The perishability of these products adds complexity to supply chain management, requiring efficient coordination of inventory and transportation decisions.

## Methodology

### Co-Solver Approach
The Co-Solver employs deterministic optimization to solve PIRP by alternating between inventory allocation and routing subproblems:
- Initial route generation using heuristics
- Inventory allocation subproblem using Gurobi
- Routing subproblem formulated as a Traveling Salesman Problem
- Dynamic weight adjustment between iterations
- Iterative optimization until convergence

### NSGA-II Approach
NSGA-II is a genetic algorithm designed for multi-objective optimization that:
- Generates a diverse set of Pareto-optimal solutions
- Balances trade-offs among conflicting objectives
- Applies Pareto dominance to identify non-dominated solutions
- Uses genetic operations (crossover and mutation) to explore the search space
- Maintains diversity using crowding distance

## Key Results
- Co-Solver solutions are on par with NSGA-II for profit and emissions metrics
- Co-Solver demonstrates significantly faster runtime (1.7s vs 37s for small test cases, 5-10 minutes vs 2-3 hours for larger test cases)
- Co-Solver is particularly suitable for large-scale or time-sensitive problems
- NSGA-II provides a broader range of trade-off solutions but requires longer computational time

## Implementation Details
The implementation includes:
- Mathematical formulation of the PIRP model
- Implementation of both Co-Solver and NSGA-II approaches
- Randomized data generation for testing
- Scalability testing with varying numbers of retailers
- Performance metrics comparison

## Future Directions
1. **Hybrid Algorithms**: Combining evolutionary methods with exact solvers
2. **Pareto Front Insights**: Enhanced analysis and visualization of multi-objective trade-offs
3. **Real-World Challenges**: Adapting models for stochastic demand and disruptions
4. **Multi-Echelon Supply Chains**: Expanding to include broader logistics networks

## Author
Likith Reddy Chintala
- MS in Operations Research and Industrial Engineering, UT Austin
- [LinkedIn](https://www.linkedin.com/in/likith-reddy-chintala-27099117a/)
- [GitHub](https://github.com/Likithreddy18)

## License
This project is licensed under the MIT License - see the LICENSE file for details.
