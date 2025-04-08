# Computational Physics
This repo documents my attempts to learn computational physics. 
This is the current list of tasks we have figured out how to do and problems we have solved

- [X] Poisson's equation $\nabla^2 V = -\frac{1}{\epsilon_0}\rho$
- [X] Wave equation $\frac{\partial^2 y}{\partial^2 t} =v^2\frac{\partial^2 y}{\partial^2 x}$
- [ ] Schrödinger's equation $-\frac{\hbar}{2m}\nabla^2 \psi +V(x) \psi = E \psi$
- [ ] Tripple pendulum

## Partial differential equations
Partial differential Equations are typically solved via the finite difference method. 
For most of the one's we have solved, we went about them by looking up formulae. 
In practice you can derive a numerical formula for the equation at hand. Typically, for a linear pde, it is of the form

$$
\Sigma_{k=0}^n\Sigma_{i=0}^m p_i(X) \frac{\partial^k f}{\partial^k X_i} =q(X)
$$

Where $X$ is all the dependent variables of the function $f$ and $X_i$ is a chosen subset of $X$ 
Then we can represent each partial derivative as its forward difference. For instance lets work with the following pde

$$
\nabla^2 f = 0 
$$

In 2 dimensions, which is called Laplace's equation.
then for any given partial derivative in the equation you can write it as its forward difference

$$
\frac{\partial^2 f}{\partial^2 x} = \frac{f_{i,j+1}-2f_{i,j}+f_{i,j+1}}{(\Delta x)^2}
$$

where the indices $i,j$ correspond to y and x respectively. It is easy to then expand on this and repeat for the rest of the derivatives.
Once a all derivatives have been substituted, you find an expression for some $f_{i,j}$ (you may want to solve for one with a plus one
depending on the equation) and iterate over all the sample points you have untill you reach a decent approcimation of the function at every
given point.


