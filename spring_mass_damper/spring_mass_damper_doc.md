# Spring mass damper


Given a spring of stiffness $k$ a damper with coefficient $c$ and a mass $m$, Newton's second law states that:

$$
m\ddot{x} = -kx - c\dot{x}.
$$

Rewriting in state space, using $v = \dot{x}$, we have that:

$$
\frac{\mathrm{d}\boldsymbol{y}}{\mathrm{d}t} = \boldsymbol{A}\boldsymbol{y}, 
$$

where

$$
\boldsymbol{y} = 
\begin{bmatrix}
x\\v
\end{bmatrix}, 
\quad
\boldsymbol{A} = 
\begin{bmatrix}
0 & 1
\\
-\dfrac{k}{m} & -\dfrac{c}{m}
\end{bmatrix}
$$

## Cost functional
At this stage it is convenient to introduce a cost functional $\mathcal{J}(\boldsymbol{y}, \boldsymbol{p})$ where $\boldsymbol{p}$ is a vector of parameters 

$$
\boldsymbol{p} = 
\begin{bmatrix}
k \\ c \\ m
\end{bmatrix}, 
$$

Examples of cost functionals are the energy of the system:

$$
\mathcal{J}(\boldsymbol{y}, \boldsymbol{p})
= \int_0^t \frac{1}{2}mv^2 + \frac{1}{2} kx^2 \ \mathrm{d}t
$$ 


## Adjoint equations
