## First Blog, Regression

Current plans: Talk about regression

Regression is a statistical tool used to determine the relationship between a set of variables. It is an elementary topic for data analytics, and is super important as it forms the basis of machine learning (by predicting outcomes using variables).

Suppose we have *N* data points. Intuitively we want to draw a line (or any polynomial) through the points that is the most "fit", that is have the points as close to the line as possible.

*Insert Picture of data points and a best fit polynomial Here*

More specifically given data points $(\vec{x}_1, y_1), (\vec{x}_2, y_2), ... , (\vec{x}_n, y_n)$, where $\vec{x}_i \in \mathbb{R}^d$, we want to find the function $f(x)$ that best fits the data.
Assuming the data fits a line, we have the following system of linear equations:

$$ y_1 = m_1x_{1,1} + m_2x_{1,2} + \cdots + m_dx_{1,d} + b $$

$$ y_2 = m_1x_{2,1} + m_2x_{2,2} + \cdots + m_dx_{2,d} + b $$

$$\vdots $$

$$ y_N = m_1x_{N,1} + m_2x_{N,2} + \cdots + m_dx_{N,d} + b $$


```


```



References: will be coming!
