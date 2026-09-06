## Monte Carlo Simulation of a Stock Portfolio

## Install Jupyter notebook (mac os)

```shell
python3 -m pip install jupyter
jupyter notebook

```
or

In vsocde, open jupyter notebook, at top right hand corner 'Select Kernel -> Python environment' (e.g. Python 3.13.7)


## What is Matrix


A **matrix** is a two-dimensional grid of numbers structured in rows and columns. In programming, matrices organize data efficiently, allowing developers to execute operations on entire datasets simultaneously rather than processing individual elements sequentially.

Replacing traditional `for` loops with matrix math—a technique known as **vectorization**—offers three primary advantages:

* **Massive Speedup:** Standard loops execute code line-by-line through a high-level interpreter, which incurs significant overhead. Matrix libraries (like NumPy) push computations to highly optimized, low-level languages like C++.
* **Hardware Efficiency:** Matrix operations leverage modern CPU capabilities, such as **SIMD** (Single Instruction, Multiple Data). This allows the hardware to calculate multiple data points in a single clock cycle while maximizing memory cache efficiency.
* **Readability:** Vectorization eliminates nested loops, boilerplate indexing, and state tracking. This condenses complex operations into single, declarative lines of code, reducing bugs and improving maintainability.

Ultimately, shifting from iterative loops to matrix operations transforms sluggish, sequential tasks into highly parallelized, lightning-fast computations.

## Matrix Multiplication Formula Example

Matrix multiplication is the most common linear algebra formula used to replace slow, nested `for` loops in modern computing.

---

### 1. The Mathematical Formula

When you multiply a **$2 \times 3$ matrix** by a **$3 \times 2$ matrix**, you multiply the elements of each **row** from the first matrix by each **column** of the second matrix, then add them up.

$$ \left[\begin{array}{ccc} a & b & c \\\\ d & e & f \end{array}\right] \times \left[\begin{array}{cc} g & h \\\\ i & j \\\\ k & l \end{array}\right] = \left[\begin{array}{cc} (ag + bi + ck) & (ah + bj + cl) \\\\ (dg + ei + fk) & (dh + ej + fl) \end{array}\right] $$

---

### 2. Concrete Example with Numbers

Let's find the top-left element ($58$) of the resulting matrix:

$$ \left[\begin{array}{ccc} \mathbf{1} & \mathbf{2} & \mathbf{3} \\\\ 4 & 5 & 6 \end{array}\right] \times \left[\begin{array}{cc} \mathbf{7} & 8 \\\\ \mathbf{9} & 10 \\\\ \mathbf{11} & 12 \end{array}\right] = \left[\begin{array}{cc} \mathbf{(1 \cdot 7 + 2 \cdot 9 + 3 \cdot 11)} & \dots \\\\ \dots & \dots \end{array}\right] = \left[\begin{array}{cc} \mathbf{58} & 64 \\\\ 139 & 154 \end{array}\right] $$


**The Math:**

$$
(1 \times 7) + (2 \times 9) + (3 \times 11) = 7 + 18 + 33 = \mathbf{58}
$$


---

### 3. Code Comparison

#### The Slow Way: Nested `for` Loops

Manually performing this math requires **three nested loops**, creating a slow $O(N^3)$ operation.
```python
for i in range(rows_A):
    for j in range(cols_B):
        for k in range(cols_A):
            result[i][j] += A[i][k] * B[k][j]
```

#### The Fast Way: Vectorized Matrix Equation

Using matrix formulas replaces all loops with a single low-level optimized command.
```python
result = A @ B  # Or np.dot(A, B)
```


## How to code Matrix in Python
[How to code matrix](https://www.geeksforgeeks.org/python/python-matrix/)

## Analysis stock portfolio by python
- [stock-portfolio.ipynb](./stock-portfolo.ipynb)


## Use quantstats python library for portfolio analysis
- [quantstats.ipynb](./quantstats.ipynb)
- [general report](./report.html)
- [strategy analysis report](./macd.html)
- [portfolio analysis report](./portfolio-report.html)

## Reference
- [Monte Carlo Simulation of a Stock Portfolio with Python](https://www.youtube.com/watch?v=6-dhdMDiYWQ)
- [Portfolio Analysis in Python with QuantStats](https://www.youtube.com/watch?v=NqnL3KB-Jrc)
- [Github Quantstats](https://github.com/ranaroussi/quantstats)


