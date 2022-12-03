---
usemathjax: true
---

## First Blog, Regression

Regression is a statistical method used to determine the relationship between a set of quantitative variables. It is an elementary topic for data analytics, and is super important as it forms the basis of machine learning (by predicting outcomes using variables).

Suppose we have *N* data points. Intuitively we want to draw a line (or any polynomial) through the points that is the most "fit", that is have the points as close to the line as possible.

*Insert Picture of data points and a best fit polynomial Here*

More specifically given data points $(\vec{x}_1, y_1), (\vec{x}_2, y_2), ... , (\vec{x}_n, y_n)$, where $\vec{x}_i \in \mathbb{R}^d$, we want to find the function $f(x)$ that best fits the data.
Let's first assume the data fits a line (or d-dimensional plane for higher dimensions) for simplicity.   We have the following system of linear equations:

$$ y_1 = m_1x_{1,1} + m_2x_{1,2} + \cdots + m_dx_{1,d} + b $$

$$ y_2 = m_1x_{2,1} + m_2x_{2,2} + \cdots + m_dx_{2,d} + b $$

$$\vdots $$

$$ y_N = m_1x_{N,1} + m_2x_{N,2} + \cdots + m_dx_{N,d} + b $$

In matrix form we have 

$$\vec{y} = A\vec{b} $$

where 

$$\vec{y} = \begin{bmatrix} y_1 \\ 
y_2 \\ 
\vdots \\
y_N
\end{bmatrix},
A = \begin{bmatrix} x_{1,1} & x_{1,2} & \cdots & x_{1,d} & 1\\
x_{2,1} & x_{2,2} & \cdots & x_{2,d} & 1\\
 &          &    \ddots    &         & \\
x_{N,1} & x_{N,2} & \cdots & x_{N,d} & 1
\end{bmatrix}
\text{and} ~
\vec{b} = \begin{bmatrix} m_1 \\
m_2 \\
\vdots \\
m_d \\
b
\end{bmatrix}
$$

If $A$ is invertible then it's straightforward to find $\vec{b}$. This also means our points lie exactly on a line. Unfortunately this will almost never happen and we have to turn to a different approach.

To make our line fit, we want to minimize the error 

$$  \min\limits_{\vec{b}}||\vec{y} - A\vec{b}||^2$$

Skipping the details, it turns out the optimal $b*$ that minimizes the error is 

$$b^* = R^{-1}Q^T\vec{y},$$

where $A = QR$ is the factorization of $A$ into $Q$, an orthogonal matrix, and $R$, and upper triangular matrix. 


Now instead of a line, lets fit our data using a quadratic polynomial, and set $d = 2$ for simplicity.

For the $d = 1$ case where both $x$ and $y$ are scalars, we have $y = m'x^2 + mx + b$ to represent our linear equations to create $A$.

For $d = 2$ we get 

$$y_i = m_1x_{i1}^2 + m_2x_{i2}^2 + m_3x_{i1}x_{i2} + m_4x_{i1} + m_5x_{i2} + b$$


References: will be coming!
