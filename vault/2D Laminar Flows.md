# 2D Laminar Flows
#note

Two big mathematical models: **Cartesian** and **axis-symmetric**

**Laminar flow**
- Fluid travels smoothly or in regular paths
- No random fluctuations
**Starting point from which we will build up 3D flows**

### Boundary Value Problem: 2D

$\vec{V}= u\hat{i}+v\hat{j}$

*Unknown Functions*
1. $u(x,y)$
2. $v(x,y)$
3. $p(x,y)$

### 2D Governing Equations: Scalar Form

$$\nabla \cdot \vec{V}=0 \Rightarrow \frac{∂u}{∂x} + \frac{∂v}{∂y}=0$$

$$\rho(\vec{V}\cdot\nabla)\vec{V}=-\nabla p+\mu\nabla^2\vec{V} \tag{Navier Stokes equations}$$

Which, in each scalar form, is:

$\rho\left(u\frac{∂u}{∂x} + v\frac{∂u}{∂y}\right)=-\frac{∂p}{∂x}+\mu\left(\frac{∂^2u}{∂x^2}+\frac{∂^2u}{∂y^2}\right)$
$\rho\left(u\frac{∂v}{∂x} + v\frac{∂v}{∂y}\right)=-\frac{∂p}{∂y}+\mu\left(\frac{∂^2v}{∂x^2}+\frac{∂^2v}{∂y^2}\right)$


### Domain for 2D Flows
- Domain is 2D
- Usually defined in the $xy$ plane

### Flows are defined in *cylindrical coordinates* $(r,\theta,z)$

$\vec{V}= v_r \hat{\mathbf{e}}_r + v_z \hat{\mathbf{e}}_z + \cancel{v_\theta \hat{\mathbf{e}}_\theta}$ (only 2D)

### Axis-Symmetric Equations

**Continuity Equations**
$\nabla\cdot\vec{V}=0$

For axis-symmetric: $\frac{1}{r}\frac{∂(rv_r)}{∂r}+\frac{∂v_z}{∂z}=0$

For 2D (as before): $\frac{∂u}{∂x}+\frac{dv}{∂y}=0$

**Momentum Equations**
As before:
$$\rho(\vec{V}\cdot\nabla)\vec{V}=-\nabla p+\mu\nabla^2\vec{V} \tag{Navier Stokes equations}$$

Therefore, we have the axis-symmetric momentum in the $z$ direction, in scalar form as:

$\rho\left(v_r\frac{∂v_z}{∂r}+v_z\frac{∂v_z}{∂z}\right)=-\frac{∂p}{∂z}+\mu\left(\frac{1}{r}\frac{∂}{∂r}\left(r\frac{∂v_z}{∂r}\right)+\frac{∂^2v_z}{dz^2}\right)$

This is similar to the 2D momentum conservation in the $x$ direction, which was:
$\rho\left(u\frac{∂u}{∂x} + v\frac{∂u}{∂y}\right)=-\frac{∂p}{∂x}+\mu\left(\frac{∂^2u}{∂x^2}+\frac{∂^2u}{∂y^2}\right)$


Therefore, in total we have **three** governing equations, which correspond to our original three unknown functions:

$$
\begin{gather*}
\frac{1}{r}\frac{∂(rv_r)}{∂r}+\frac{∂v_z}{∂z}=0 \\
\rho\left(v_r\frac{∂v_z}{∂r}+v_z\frac{∂v_z}{∂z}\right)=-\frac{∂p}{∂z}+\mu\left(\frac{1}{r}\frac{∂}{∂r}\left(r\frac{∂v_z}{∂r}\right)+\frac{∂^2v_z}{dz^2}\right) \\
\rho\left(v_r\frac{∂v_r}{∂r}+v_z\frac{∂v_r}{∂z}\right)=-\frac{∂p}{∂r}+\mu\left(\frac{1}{r}\frac{∂}{∂r}\left(r\frac{∂v_r}{∂r}\right)-\frac{v_r}{r^2}+\frac{∂^2v_r}{∂z^2}\right) \\
\end{gather*}
$$


Which allow us to solve the unknown functions $v_r(r,z)$, $v_z(r,z)$, and $p(r,z)$.
