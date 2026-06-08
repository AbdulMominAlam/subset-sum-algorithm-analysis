# Subset Sum Algorithm Analysis

This project investigates the NP-Complete Subset Sum problem using both exact and heuristic approaches.

## Problem Description

Given a set of positive integers and a target value T, determine whether a subset exists whose sum equals T. The optimization version seeks the subset with the maximum sum not exceeding T.

## Algorithms Implemented

### Brute Force
- Examines every possible subset
- Always returns the optimal solution
- Time Complexity: Θ(n · 2ⁿ)

### Greedy Heuristic
- Sorts elements in descending order
- Iteratively selects feasible elements
- Time Complexity: Θ(n log n)
- Produces near-optimal solutions but is not always optimal

## Experimental Analysis

### Performance Testing
- Input sizes up to n = 10,000
- 90% confidence intervals
- All b/a values below 0.1
- Experimental results confirmed Θ(n log n)

### Quality Testing
- Compared greedy results against optimal brute force solutions
- Mean quality ratio remained above 0.968
- Best observed quality ratio: 0.9969

### Functional Testing
- Black-box testing
- White-box testing
- Equivalence class testing
- Boundary value testing

All functional tests passed successfully.

## Authors

- Abdul Momin Alam
- Abdallah Al Homsi
- Rand Mo Khaled

Sabancı University
CS301 Algorithms
Spring 2025–2026
