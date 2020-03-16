# Quadratic Function

## $2\times2$ Matrix
Let $A \in \mathbb{R}^{2\times2}$ and $x \in \mathbb{R}^2$, with $A$ symmetric and positive definite.

Then 
\begin{align}
x^T A x &= [x_1 x_2] \begin{bmatrix} a_{11} & a_{12} \\ a_{12} & a_{22} \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix}\\
&= a_{11}x_1^2 + 2 a_{12} x_1 x_2 + a_{22} x_2^2
\end{align}

and if $x$ is a function of time, $x(t)$ then $\dot{x} = \frac{d x}{dt}$ is

$$
\dot{x} = 2a_{11}x_1 \dot{x_1} + 2 a_{12} x_1 \dot{x_2} + 2 a_{12} x_2 \dot{x_1} + 2a_{22} x_2\dot{x_2}
$$