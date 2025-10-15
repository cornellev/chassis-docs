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


$u$ = velocity $\left(\pu{\frac{m}{s}}\right)$
$\rho$ = density $\left(\pu{\frac{kg}{m^3}}\right)$
$\mu$ = viscosity $\left(\pu{\frac{kg}{m\times s}}\right)$
$p$ = pressure $\left(\pu{\frac{N}{m^2}}\right)$
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

Steady Flow: $p(x,y,t)=p(x,y)$, and $\mathbf{V}(x,y,t)=\mathbf{V}(x,y)=u(x,y)\hat{\mathbf{i}}+v(x,y)\hat{\mathbf{j}}$

**Lagrangian**
At time $t_0$, fluid element "$A$" is at $(x_0, y_0)$
- $x_A(t_0)=x_0$
- $y_A(t_0)=y_0$
- $\mathbf{V}_A(t_0)=\mathbf{V}_0=u_0\hat{\mathbf{i}}+v_0\hat{\mathbf{j}}$

### Differential Form of Mass Conservation
- $\rho$ = constant (incompressible flow)
- mass = $\rho * Volume$
Go from time $t$ to $t+\Delta t$ and let $\Delta t \rightarrow 0$ 
- $\Delta Vol=\Delta u\Delta t\Delta y\Delta z$ 
- $\frac{\Delta Vol}{\Delta t Vol}=\frac{∂u}{∂x}+\frac{∂v}{∂y}$ 
- $\Delta u=\frac{∂u}{∂x} \Delta x +h.o.t.$ 
- $\Delta v=\frac{∂v}{∂y}\Delta y$

### Differential Form of Momentum Conservation
**Forces
- Pressure
- Viscous
- ~~Gravity~~
- $a_x=\lim_{\Delta t \to 0} \frac{\Delta u}{\Delta t}=u \frac{∂u}{∂x}+v \frac{∂u}{∂y}$
- $a_y=\lim_{\Delta t \to 0} \frac{\Delta v}{\Delta t}=u \frac{∂v}{∂x}+v \frac{∂v}{∂y}$
**Acceleration in 2D
$$\vec{a}=\left(u \frac{∂u}{∂x}+v \frac{∂u}{∂y}\right)\hat{\mathbf{i}}+\left(u \frac{∂v}{∂x}+v \frac{∂v}{∂y}\right)\hat{\mathbf{j}}$$  
**Other forms
- $\vec a=\left(\vec V \cdot \nabla \right)$ where $\vec V=u\hat{\mathbf{i}}+v\hat{\mathbf{j}}$  and $\nabla = \hat{\mathbf{i}} \frac{∂}{∂x}+\hat{\mathbf{j}}\frac{∂}{∂y}$ 
**Pressure Force on Fluid Element
- Net pressure force in x dir. per unit volume = $-\frac{∂p}{∂x}$
- Net pressure force in y dir. per unit volume = $-\frac{∂p}{∂y}$
- Net pressure force per unit volume:
$$-\left(\frac{∂p}{∂x}\hat{\mathbf{i}}+\frac{∂p}{∂y}\hat{\mathbf{j}}\right)=-\nabla p$$
**Viscous Forces
![Viscous Forces](Images/Viscous-Forces.png)
- Net viscous forces per unit volume:
$$\left(\frac{∂\tau_{xx}}{∂x}+\frac{∂\tau_{xy}}{∂y}\right)\hat{\mathbf{i}}+\left(\frac{∂\tau_{xy}}{∂x}+\frac{∂\tau_{yy}}{∂y}\right)\hat{\mathbf{j}}$$
- $\hat{\mathbf{i}}$ is forces in x and $\hat{\mathbf{j}}$ is forces in y

**Forces per unit volume 
- Net pressure force per unit volume:$$-\left(\frac{∂p}{∂x}\hat{i}+\frac{∂p}{∂y}\hat{j}\right)=-\nabla p$$
- Net viscous force per unit volume:$$\left(\frac{∂\tau_{xx}}{∂x}+\frac{∂\tau_{xy}}{∂y}\right)\hat{\mathbf{i}}+\left(\frac{∂\tau_{xy}}{∂x}+\frac{∂\tau_{yy}}{∂y}\right)\hat{\mathbf{j}}=\nabla \cdot \mathbf{\tau}$$$$\nabla \cdot \mathbf{\tau}=\begin{bmatrix} \dfrac{∂}{∂x}&\dfrac{∂}{∂y}\end{bmatrix} \cdot \begin{bmatrix} \tau_{xx} & \tau_{xy} \\ \tau_{xy} & \tau_{yy}\end{bmatrix}$$
**Differential Form of Momentum Conservation**
$\rho \left(\vec{V} \cdot \nabla \right)\vec{V}=-\nabla p+\nabla \cdot \mathbf{\tau}$
$\rho \left(u \dfrac{∂u}{∂x}+v \dfrac{∂u}{∂y}\right)=-\dfrac{∂p}{∂x}+\dfrac{∂\tau_{xx}}{∂x}+\dfrac{∂\tau_{xy}}{∂y}$ 
$\rho \left(u \dfrac{∂v}{∂x}+v \dfrac{∂v}{∂y}\right)=-\dfrac{∂p}{∂y}+\dfrac{∂\tau_{xy}}{∂x}+\dfrac{∂\tau_{yy}}{∂y}$ 

Unknown functions:
- $u(x,y)$
- $v$
- $p$
- $\tau_{xx}$
- $\tau_{xy}$
- $\tau_{yy}$

**Newtonian Fluids**
![Newtonian Fluid](Images/Newtonian_Fluid1.png)
![Newtonian Fluid](Images/Newtonian_Fluid2.png)
![Newtonian Fluid](Images/Newtonian_Fluid3.png)
- If you preform $\vec{F}=m\vec{a}$ on a Newtonian Fluid, you get the **Navier-Stokes equations**:
$$\rho \left(u \dfrac{∂u}{∂x}+v \dfrac{∂u}{∂y}\right)=-\dfrac{∂p}{∂x}+\mu\left(\dfrac{∂^2u}{∂x^2}+\dfrac{∂^2u}{∂y^2}\right)$$$$\rho \left(u \dfrac{∂v}{∂x}+v \dfrac{∂v}{∂y}\right)=-\dfrac{∂p}{∂y}+\mu\left(\dfrac{∂^2v}{∂x^2}+\dfrac{∂^2v}{∂y^2}\right)$$
**These equations are what's used to solve for the state of a fluid element at time t**

**Unknowns**:
- $u(x,y)$
- $v(x,y)$
- $p(x,y)$

**Assumptions**
- 2D
- Steady
- Newtonian Fluid
	- $\tau=\mu\dot{\gamma}$ and $\mu$ is constant
- Incompressible

