# CFD: Mathematical Model
#note

### Boundary Value Problem
(Continued from "What's inside the black box")

**Simple BVP**
Determine $u(x)$ such that $\frac{d^2u}{dx^2}=1$ and $0\leq x \leq 4$

**Governing equations are derived using fundamental laws of fluid flow**
- Conservation of mass
- Conservation of momentum: $\mathbf{F}=m\mathbf{a}$
- But *not* conservation of energy

$$\rho\left(u\frac{∂u}{∂x}+v\frac{∂u}{∂y}\right)=-\frac{∂p}{dx}+\mu\left(\frac{∂^2u}{∂x^2}+\frac{∂^2u}{∂y^2}\right)$$

### Differential and Integral Forms of Governing Equations

**Differential**: Apply conservation laws to infinitesimal fluid element
- Just like we have an infinitesimal displacement "$ds$" for work, the we have the same thing here, but instead is $dV$.

**Integral**: Apply conservation laws to finite region in flow domain

### Eulerian and Lagrangian Descriptions

**Velocity and Pressure Field**
- $\mathbf{V}(x,y,t)$
- $p(x,y,t)$

**Eulerian**
At time $t_0$, velocity at $(x_0,y_0)$ is $\mathbf{V}(x_0,y_0,t_0)=\mathbf{V}_0$

Steady Flow: $p(x,y,t)=p(x,y)$, and $\mathbf{V}(x,y,t)=\mathbf{V}(x,y)$

