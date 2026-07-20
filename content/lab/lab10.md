---
title: "Lab10"
author: "Wonjun Seo"
summary: "Optimization"
draft: true
---
## Numerical Methods

### Solving Equations

#### 1. Bisection Method
> When does the bisection method fail?
#### 2. Newton's Method
**Counterexamples**
- (a) $f(x) = x^2 - 2$, $x_0 = 0$.
- (b) $f(x) = x^3 - 2x + 2$, $x_0 = 0$.
- (c) $f(x) = x^3 -x$, $x_0 = 0.5$ vs. $x_0 = 0.6$.
- (d) $f(x) = x^{1/3}$, $x_0 = 2$.
- (e) $f(x) = \ln (x) \cdot \exp \left ( \sin \left (\sqrt{x^2+1} \right ) + \frac{x^x}{1 + \ln (x^2 + 1)} \right )$, $x_0 = 2$.

### Optimization

#### Gradient Descent