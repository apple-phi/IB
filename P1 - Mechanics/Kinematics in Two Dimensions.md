## Moment of inertia
The centre of mass of a rigid body is usually denoted $G$.
$$
\mathbf{v}_{g}=\int \mathbf{v}_{i} \, \mathrm{d}m 
$$
The weight force acts vertically down through $G$.

The moment of inertia is defined as 
$$
I=\int r^{2} \, \mathrm{d}m 
$$
### The perpendicular axis theorem
For a lamina with the $z$ axis perpendicular to the plane,
$$
I_{zz}=I_{xx}+I_{yy}
$$
### The parallel axis theorem 
The moment of inertia around an axis displaced from $G$ by a distance $r$ is related to it’s parallel axis through $G$ by
$$
I'=I_{g}+mr^{2}
$$
### The radius of gyration
If the body was concentrated at a specific radius around the centre of rotation, the *radius of gyration* that gives the same moment of inertia as the original body is denoted $k=r_{g}$ such that
$$
I=mk^{2}
$$
>Note the relationship with random walks from a given seed point—there is a similar [[Elasticity of compliant materials#Random walk|radius of gyration]] in that context.

### Rotation
$$
\begin{cases}
\begin{align}
T & =I\ddot{\theta} \\
U & = \frac{1}{2}I\dot{\theta}^{2}
\end{align}
\end{cases}
$$
>Note that the IB course recommends to always use the centre of mass as the centre of rotation. This is because most people don’t use their brains and forget to add the extra terms due to relative motion…

It is useful to recall that
$$
\ddot{\theta}=\dot{\theta} \frac{ \mathrm{d} \dot{\theta} }{ \mathrm{d} \theta } =\frac{1}{2} \frac{\mathrm{d}( \dot{\theta}^{2} )}{\mathrm{d} t}
$$

## d’Alembert’s principle
In an accelerating reference frame, the stationary acceleration manifests itself as forces $-m\mathbf{a}$ and torques $-I\dot{\theta}$.

>The centripetal force is an example of one of these “fictitious” forces. Calling them fictitious is a bit of a misnomer, however, because the laws of physics are the same in every reference frame, *á la* relativity. (This is Einstein’s equivalence principle).

## Linear and angular momentum
Linear momentum and angular momentum around a point are always conserved in stationary reference frames.

An *impulse* is a change in a momentum
$$
\mathbf{p}_{i}=\Delta(m\mathbf{v})=\mathbf{f}t
$$
>Finite forces are considered negligible compared to impulse forces.

The angular momentum generated by an impulse is
$$
\Delta \mathbf{h}=\mathbf{r}\times \mathbf{p}=\Delta(I\mathbf{\boldsymbol{\omega}})
$$
## Example
Consider a pencil length $2a$ which is dropped horizontally a height $h$ before it clips the edge of a table in an elastic collision. Find how far down the side of the table it collides again with the table.

Before:
$$
\begin{align}
u=\sqrt{ 2gh } \\
h_{p}=m ua \\
\mathrm{KE}=\frac{1}{2}mu^{2}
\end{align}
$$
After:
$$
\begin{align}
h_{p} & = mva+ \frac{1}{3}ma^{2}\omega\\
 & = \frac{1}{2}v^{2}+ \frac{1}{2} \frac{1}{3}ma^{2}\omega^{2} \\
 \\
 & \begin{cases}
\begin{aligned}
a\omega^2  & =3(u-v) \\
\underbrace{ u^{2}-v^{2} }_{ (u-v)(u+v) } & = \frac{1}{3}(a\omega)^{2}

\end{aligned}
\end{cases} \\
\Rightarrow\quad  v & =\frac{u}{2} \quad\text{s.t.}\quad a\omega= \frac{3}{2} \\
 \\
t=\frac{\pi}{\omega} & = \frac{2\pi a}{3u} \\
x & = vt+\frac{1}{2}at^{2} \\
 & =3a
\end{align}$$
## Rotating unit vectors
In general,
$$
\dot{\mathbf{e}}= \dot{\mathbf{\theta}}\times \mathbf{e}
$$
### Polar coordinates
Applying the product rule to the definition of polar $\mathbf{r}$,
$$
\begin{align}
\mathbf{r} & =r\,\mathbf{e}_{\theta} \\
\dot{\mathbf{r}} & = \dot{r}\,\mathbf{e}_{r}+r\dot{\theta}\,\mathbf{e}_{\theta} \\
\ddot{\mathbf{r}} & = (\underbrace{ \ddot{r} }_{ \mathrm{radial} }- \underbrace{ r\dot{\theta}^{2} }_{ \mathrm{centripet al} })\,\mathbf{e}_{r}+(\underbrace{ 2\dot{r}\dot{\theta} }_{ \text{Coriolis} }+\underbrace{ r \ddot{\theta} }_{ \mathrm{tan gential} })\,\mathbf{e}_{\theta}
\end{align}
$$


## Equations of motion
Consider a particle sliding without friction along a rod that turns at angular speed $\omega$.
### Case 1: constant angular speed
$$
\begin{align}
\ddot{\mathbf{r}} & =(\ddot{r}-r\dot{\theta}^{2})\mathbf{e}_{r}+(2\dot{r}\dot{\theta} +r \ddot{\theta})\mathbf{e}_{\theta}   \\
 & =(2\dot{r}\dot{\theta} +r \ddot{\theta})\mathbf{e}_{\theta} \\
 \\
 & \Rightarrow\quad   \boxed{\ddot{r}-r\dot{\theta}^{2} =0}
\end{align}
$$

### Case 2: no torque at rod CoR
Similarly,
$$
\begin{align}
\ddot{\mathbf{r}} & =(\ddot{r}-r\dot{\theta}^{2})\mathbf{e}_{r}+(2\dot{r}\dot{\theta} +r \ddot{\theta})\mathbf{e}_{\theta}   \\
& =(\ddot{r}-r\dot{\theta}^{2})\mathbf{e}_{r}\\
 \\
 & \Rightarrow\quad   \boxed{2\dot{r}\dot{\theta} +r \ddot{\theta} =0}
\end{align}
$$