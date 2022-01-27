---
author: "Lucas LaValva"
date: "January 28, 2022"
title: "LaTeX Practice"
---

# Assigned Equation
$$
\int_0^{\tanh(1)}\prod_{i=1}^\infty \frac{\nabla f(\zeta)}{1-p_i^\zeta}d\zeta
$$

# Interesting Equations
### Fun Recursive Differential Equation
$$
  f'(x) = \frac{f(x)}{1 + \frac{f(x)}{1 + \frac{f(x)}{1 + \ldots}}}
$$

### Chebyshev Nodes
$$
    x_k = \cos\left(\frac{2\pi(n-k)}{2n+1}\right)
$$

### Fibonacci Generator
$$
  \begin{bmatrix}
    F_n \\
    F_{n-1}
  \end{bmatrix}
  =
  \begin{bmatrix}
    1 & 1 \\
    1 & 0
  \end{bmatrix}
  \begin{bmatrix}
    F_{n-1} \\
    F_{n-2}
  \end{bmatrix}
$$

### The Pythagorean Theorem
$$
  a^2 + b^2 = c^2
$$

# Code for this paper (Markdown with $LaTeX$)

````markdown
---
author: "Lucas LaValva"
date: "January 28, 2022"
title: "LaTeX Practice"
---

# Assigned Equation
$$
\int_0^{\tanh(1)}\prod_{i=1}^\infty \frac{\nabla f(\zeta)}{1-p_i^\zeta}d\zeta
$$

# Interesting Equations
### Fun Recursive Differential Equation
$$
  f'(x) = \frac{f(x)}{1 + \frac{f(x)}{1 + \frac{f(x)}{1 + \ldots}}}
$$

### Chebyshev Nodes
$$
    x_k = \cos\left(\frac{2\pi(n-k)}{2n+1}\right)
$$

### Fibonacci Generator
$$
  \begin{bmatrix}
    F_n \\
    F_{n-1}
  \end{bmatrix}
  =
  \begin{bmatrix}
    1 & 1 \\
    1 & 0
  \end{bmatrix}
  \begin{bmatrix}
    F_{n-1} \\
    F_{n-2}
  \end{bmatrix}
$$

### The Pythagorean Theorem
$$
  a^2 + b^2 = c^2
$$

# Code for this document (Markdown with $LaTeX$)

```markdown
  (Removed to prevent the document from recursing infinitely)
```
````