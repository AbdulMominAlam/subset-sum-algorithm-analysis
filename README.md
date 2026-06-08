# Subset Sum Algorithm Analysis

## Overview

This project investigates the classical **Subset Sum Problem**, one of the most well-known NP-Complete problems in computer science.

The objective is to determine whether a subset of a given set of positive integers can produce a target sum, or alternatively, to find the subset whose sum is as close as possible to the target without exceeding it.

The project compares two different approaches:

1. **Brute Force Algorithm (Exact)**
2. **Greedy Heuristic Algorithm (Approximate)**

In addition to implementing both algorithms, the project includes theoretical complexity analysis, experimental performance testing, solution quality evaluation, and functional testing.

---

## Problem Definition

Given:

```
S = {a₁, a₂, ..., aₙ}
```

and a target value:

```
T
```

Determine whether there exists a subset:

```
S′ ⊆ S
```

such that:

```
Σ aᵢ = T
```

### Example

Input:

```
S = {3, 5, 7, 10}
T = 15
```

Output:

```
YES
```

because:

```
5 + 10 = 15
```

---

## Decision vs Optimization Versions

### Decision Version

Determine whether an exact solution exists.

```
Does there exist a subset whose sum equals T?
```

Output:

```
YES / NO
```

### Optimization Version

Find the subset with the largest possible sum that does not exceed the target.

```
maximize subset_sum ≤ T
```

---

## Algorithms Implemented

### 1. Brute Force Algorithm

The brute force approach generates every possible subset and evaluates each one.

#### Advantages

- Always finds the optimal solution
- Guarantees correctness

#### Disadvantages

- Extremely slow for larger inputs
- Exponential growth

#### Complexity

Time:

```
Θ(n · 2ⁿ)
```

Space:

```
O(n)
```

---

### 2. Greedy Heuristic Algorithm

The greedy approach:

1. Sorts elements in descending order
2. Iteratively adds elements if they do not exceed the target

#### Advantages

- Very fast
- Scales to large inputs

#### Disadvantages

- Does not always return the optimal solution

#### Complexity

Time:

```
Θ(n log n)
```

Space:

```
O(n)
```

---

## Experimental Methodology

The project evaluates both algorithms using randomly generated test instances.

### Generator Parameters

| Parameter | Description |
|------------|------------|
| n | Number of elements |
| min_value | Minimum element value |
| max_value | Maximum element value |
| target_ratio | Target as a percentage of total sum |
| seed | Random seed |

---

## Performance Testing

The objective was to experimentally verify the practical running time of the greedy heuristic.

### Input Sizes

```
n = 50
n = 100
n = 200
n = 400
n = 800
n = 1600
n = 3200
n = 6400
n = 10000
```

### Statistical Analysis

For each input size:

- Multiple measurements were collected
- 90% confidence intervals were computed
- Measurements continued until:

```
b / a < 0.1
```

where:

- a = mean running time
- b = confidence interval half-width

This follows the methodology required by the course project specification.

### Results

Experimental results confirmed:

```
Θ(n log n)
```

behavior for the greedy heuristic.

---

## Quality Testing

The greedy algorithm was compared against the optimal brute force solution.

### Quality Ratio

Defined as:

```
Quality Ratio =
Greedy Solution Sum
-------------------
Optimal Solution Sum
```

A value of:

```
1.0
```

indicates perfect optimality.

### Results

- Mean quality ratio always exceeded 0.968
- Best observed quality ratio: 0.9969
- Mean percentage gap remained below 3%

These results indicate that the greedy heuristic consistently produces near-optimal solutions.

---

## Functional Testing

Several testing techniques were applied to verify implementation correctness.

### Black-Box Testing

Tests designed from the problem specification without examining the source code.

Examples:

- Target = 0
- Exact subset exists
- No exact subset exists
- All elements larger than target

### White-Box Testing

Tests designed using knowledge of the implementation.

Examples:

- Add branch execution
- Skip branch execution
- Exact match branch
- Non-optimal greedy behavior

### Equivalence Class Testing

Input classes included:

- Exact solution exists
- No exact solution exists
- Duplicate values
- Single-element inputs
- All values exceed target

### Results

All functional tests passed successfully.

---

## Repository Structure

```
subset-sum-algorithm-analysis
│
├── CS301_Project_Codes.ipynb
├── CS301_Project_Report_Group_26.pdf
├── CS301_Group26_Presentation.pptx
│
├── section6_mean_time_plot.png
├── section6_fitted_line_plot.png
├── section6_log_log_plot.png
│
├── section7_quality_ratio_plot.png
├── section7_greedy_optimal_rate_plot.png
│
├── section6_performance_results.csv
├── section7_quality_results.csv
├── section8_functional_testing_results.csv
└── README.md
```

---

## Key Findings

✅ Subset Sum is NP-Complete

✅ Brute Force always returns the optimal solution

✅ Greedy heuristic runs in Θ(n log n)

✅ Experimental results matched theoretical analysis

✅ Quality ratios remained above 0.968

✅ All functional tests passed

---

## Authors

**Abdul Momin Alam**

**Abdallah Al Homsi**

**Rand Mo Khaled**

Sabancı University  
CS301 – Algorithms  
Spring 2025–2026

---

## License

MIT License
