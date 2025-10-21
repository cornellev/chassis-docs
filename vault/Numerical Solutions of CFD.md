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
- **Apply mass and momentum conservation to each cell**
	- Use integral form of conservation equation
	- Interpolate cell center values to get values at the control surfaces
	- At boundaries, use boundary conditions
$$\int_{S}\vec{V} \cdot \hat{n}\,dS$$
### Order or accuracy
$u_{1-2}=\dfrac{u_{1}+u_{2}}{2}+Error2$
Using Taylor series, we get
$u{1-2}=\frac{u{1}+u_{2}}{2}+0.5\left(\dfrac{∂^2u}{∂x^2}\right)_{1-2}\left(\frac{\Delta x}{2}\right)^2+...$ 
Second-order accurate                 Error $\propto \Delta x^2$ 

### Additional Complication: Algebraic equations are nonlinear
**Momentum eq. has nonlinear terms
$\int_{S} \rho\vec{V}\left(\vec{v}\cdot\hat{n}\right)\,dS=-\int_{S} p\hat{n}\,DS+\vec{F}_{visc}$ 

**How to solve nonlinear systems?**
	- Linearize about guess values
	- Solve iteratively

### Linearization
Linearize $u_{1}^2$ using Newton's method
$u=u_{g}+\Delta u$
$f(u)=f(u_{g}+\Delta u)$ 
	$=f(u_{g})+\Delta u f'(u_{g})+\frac{\Delta u^2}{2}f''(u_{g})$
$f(u)=u^2$
$f'(u)=2u$

### Solution Process
- Iterate the solution until residuals are below our set tolerance
- Aggregate imbalance or residual
   $R=\frac{\Sigma |R_{i}|}{Scaling factor}$ 

### Algorithm
![Algorithm](images/Algorithm.png)

### Extension to Irregular Meshes
- **Cells can be any type of**
	- Polygon in 2D
	- Polyhedron in 3D
- **Calculate fluxes and forces face by face**
	- Use neighboring cell center values to get face values