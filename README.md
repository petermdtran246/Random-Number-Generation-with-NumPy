# Random Number Generation with NumPy

This exercise demonstrates how to generate reproducible random numbers using NumPy’s modern random number generator API.

The goal is to create a list of random ages while ensuring results can be reproduced across different runs and environments.

---

## Problem Description

Create an array called `random_ages` that contains **100 random integers**, where:

- Each value represents an age
- Ages range from **1 to 100 (inclusive)**
- A fixed random seed is used to ensure **reproducibility**

---

## Tools & Libraries

- Jupyter
- NumPy (`numpy.random.default_rng`)

---

## Key Concepts Practiced

- Using `default_rng()` instead of legacy NumPy random functions
- Setting a seed for reproducible results
- Generating random integers with inclusive bounds
- Understanding exclusive upper bounds in random number generation

---

## Example Code

```python
import numpy as np
from numpy.random import default_rng

rng = default_rng(12345)
random_ages = rng.integers(1, 101, size=100)

print(random_ages)
