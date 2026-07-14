---
title: "Lab07"
author: "Wonjun Seo"
summary: "Linear Regression, PCA, and Mini Project 2"
---
## MATH!
Details on linear regression and principal component analysis (PCA).

## Mini Project 2!

### Goal
In this mini project, your group will divide California into a small number of **real-estate market regions**: areas that are both geographically contiguous and similar in price. The chosen method is **$K$-means clustering**, run on the California Housing dataset using only three features: **longitude, latitude, and median house value**. 

**The goal of this mini project is to produce a written report** (there is no presentation). **The emphasis of this report is a clear explanation of the chosen method ($K$-means) and why it is appropriate for this goal.**

### Data
Run the following code to acquire California Housing dataset.

```python
import pandas as pd
from sklearn.datasets import fetch_california_housing

data = fetch_california_housing(as_frame=True)
df = data.frame
```

To see the description of the dataset, run
```python
print(data.DESCR)
```

### Instruction
Your report should contain:

1. **Detailed explanation of the methodology ($K$-means)**
   - State the purpose of the method.
   - Describe the data structure it operates on.
   - Formulate the minimization problem.
   - Describe the algorithm to solve the minimization problem.
   - Identify the hyperparameters and explain how you choose them.
   - Explain why scaling is required.
    > You may use Codex for this, but do not copy and paste directly. **Please review it carefully, make sure you fully understand it, and write in your words**.

2. **Results (figure) and interpretation**
   - Produce a final map: a **scatter plot** with **longitude on the x-axis, latitude on the y-axis, and points colored by cluster**.
   - Report each region's mean price.
   - Interpret the resulting regions.
3. **Code**: Include your full, runnable code in an **appendix**. No code chunk in main body of the report.
4. **(Optional) Try other clustering methods and compare the results**.