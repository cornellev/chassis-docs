# CFD: Numerical Solutions Strategy

### 2D Mathematical Model (review)
$$\dfrac{\partial u}{∂x}+\dfrac{∂v}{∂y}=0$$$$\rho \left(u \dfrac{∂u}{∂x}+v \dfrac{∂u}{∂y}\right)=-\dfrac{∂p}{∂x}+\mu\left(\dfrac{∂^2u}{∂x^2}+\dfrac{∂^2u}{∂y^2}\right)$$$$\rho \left(u \dfrac{∂v}{∂x}+v \dfrac{∂v}{∂y}\right)=-\dfrac{∂p}{∂y}+\mu\left(\dfrac{∂^2v}{∂x^2}+\dfrac{∂^2v}{∂y^2}\right)$$
**Unknown Functions**
1. $u(x,y)$
2. $v(x,y)$
3. $p(x,y)$

### Discretization
- Divide domain into multiple control volumes or "cells"
- Reduce problem to determining velocity and pressure at cell centers
- Interpolate cell center values to find values at other locations in cell
**How do we determine cell center values?**
- Set up system of algebraic equations in cell center values
	- Invert to get cell center values
- Do post processing to get $p(x,y)$,$u(x,y)$, etc.
### How do we derive system of algebraic equations?
