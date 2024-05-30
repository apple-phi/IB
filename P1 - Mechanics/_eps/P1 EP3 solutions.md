## 1.
- A seesaw has 1 DOF
- A cylinder rolling down a plane has 3 DOF (2 spatial, 1 rotational)
- A pair of glasses has 7 DOF (3 spatial, 2 bulk rotational, 2 internal rotational)
- A spinning chair on the floor has 4 DOF (2 spatial, 2 rotational)
- Mechanism 1 has 1 DOF
- Mechanism 2 has 0 DOF
- Mechanism 3 has 2 DOF

## 2.
By similar triangles, the fraction of $T$ that resolves along the $x$ and $y$ axes are $\frac{x}{l}$ and $\frac{y}{l}$ respectively. Then balancing forces in the $x$ and $y$ direction gives
$$
\begin{align}
-\frac{x}{l}T&=m\ddot{x} \\
-mg-\frac{y}{l}T&=m\ddot{y}
\end{align}
$$
Converting to polar coordinates, first take the expression for $x$ force balance.
$$
\begin{align}
-T\sin\theta&=ml\frac{ \mathrm{d}^{2} }{ \mathrm{d}t^{2} } \sin\theta \\
&=ml\frac{\mathrm{d} }{\mathrm{d}t} \dot{\theta}\cos\theta \\
&=ml(\ddot{\theta}\cos\theta-\dot{\theta}^{2}\sin\theta)
 \end{align}
$$
Then considering the expression for the $y$ force balance,
$$
\begin{align}
-mg+T\cos\theta&=-ml\frac{ \mathrm{d}^{2} }{{ \mathrm{d}t }^{2}}\cos\theta \\
&=ml\frac{\mathrm{d} }{\mathrm{d}t} \dot{\theta}\sin\theta \\
&=ml(\ddot{\theta}\sin\theta+\dot{\theta}^{2}\cos\theta)
 \end{align}
$$
By multiplying the first equation by $\sin \theta$ and the second by $\cos\theta$ and subtracting,
$$
-mg\cos\theta+T=ml\dot{\theta}^{2}
$$
Substituting in the $x$ force balance gives
$$
\begin{align}
-mg\cos\theta \sin\theta+\overbrace{ T\sin\theta}^{ ml(-\ddot{\theta}\cos\theta+\dot{\theta}^{2}\sin\theta) }&=ml\dot{\theta}^{2}\sin\theta \\
\Rightarrow\quad l\ddot{\theta}&=-g\sin\theta
\end{align}
$$
which is the equation of motion.

## 3.
The moment of inertia about the pivot is
$$
\begin{align}
I&=\overbrace{ \frac{ma^{2}}{12}}^{ I_{xx} }+\overbrace{ \frac{ma^{2}}{12}}^{ I_{yy} }+m\overbrace{ \left( \frac{a\sqrt{ 2 }}{2} \right)^{2}}^{ \parallel\mathrm{-axis} } \\
&=\frac{2}{3}ma^{2}
 \end{align}
$$
The kinetic energy is
$$
\begin{align}
T(\dot{\theta})&=\frac{1}{2}I\dot{\theta}^{2} \\
&=\frac{1}{3}ma^{2}\dot{\theta}^{2}
 \end{align}
$$
Taking the downwards vertical to be at $\theta=0,$ the potential energy is
$$
\begin{align}
V(\theta)&=mga\sqrt{ 2 }(1-\cos\theta)
 \end{align}
$$
Then the Lagrangian is
$$
\mathcal{L}(\theta, \dot{\theta})=\frac{1}{3}ma^{2}\dot{\theta}^{2}+mga\sqrt{ 2 }(\cos\theta-1)
$$
Then the angular momentum is
$$
\begin{align}
p_{\theta}&=\frac{\mathrm{d} \mathcal{L}}{\mathrm{d}\dot{\theta}} \\
&= \frac{2}{3}ma^{2}\dot{\theta}
 \end{align}
$$
and the torque is
$$
\begin{align}
F_{\theta}&=\frac{\mathrm{d} \mathcal{L}}{\mathrm{d}\theta}  \\
&=-mga\sqrt{ 2 }\sin\theta
 \end{align}
$$
Hence the equation of motion given by $\dot{p}_{\theta}=F_{\theta}$ is
$$
\frac{2}{3}a\ddot{\theta}=-g\sqrt{ 2 }\sin\theta
$$
For small oscillations with $\theta \approx \sin\theta,$
$$
\ddot{\theta}=-\frac{3g}{a\sqrt{ 2 }}\sin\theta
$$
This has angular frequency
$$
\omega=\sqrt{ \frac{3g}{a\sqrt{ 2 }} }
$$
so the time period is
$$
T= \frac{2\pi}{\omega}=2\pi \sqrt{ \frac{a\sqrt{ 2 }}{3g} }
$$
## 4.
For the two masses, the (appropriately scaled) Lagrangian $\mathcal{L}=T-V$ is
$$
\begin{align}
\mathcal{L}(x_{1},x_{2},\dot{x}_{1},\dot{x}_{2})&=m\dot{x}_{1}^{2}+M\dot{x}_{2}^{2}-kx_{1}^{2}-k(x_{2}-x_{1})^{2} \\
 \end{align}
$$
The generalised momenta $p_{i}=\partial_{\dot{x}_{i}}\mathcal{L}$ are
$$
\begin{align}
p_{1}&=2m\dot{x}_{1} \\
p_{2}&=2M\dot{x}_{2}
\end{align}
$$
and these are proportional to the linear momenta.

The generalised forces $F_{i}=\partial_{x_{i}}\mathcal{L}$ are
$$
\begin{align}
F_{1}&=-2kx_{1}+2k(x_{2}-x_{1}) \\
&=2kx_{2} \\
F_{2}&=-2k(x_{2}-x_{1})
\end{align}
$$
and these are proportional to the net forces acting on each of the two masses.

For the system of two disks with torsional springs of torsional spring constant $\kappa,$ the appropriately scaled Lagrangian is
$$
\mathcal{L}(\theta_{1},\theta_{2},\dot{\theta}_{1}, \dot{\theta}_{2})=I_{1}\dot{\theta}_{1}^{2}+I_{2}\dot{\theta}_{2}^{2}-\kappa\theta_{1}^{2}-\kappa(\theta_{2}-\theta_{1})^{2}
$$
This is identical to the previous Lagrangian under mapping $(m,M,k)\mapsto(I_{1},I_{2},\kappa).$ Hence the equations of motion will be identical.

The new generalised momenta will be proportional to the angular momenta and the new generalised forces will be proportional to the net torques on each disk. 

## 5.
The Lagrangian is
$$
\mathcal{L}(r,\theta,\dot{r},\dot{\theta})= \frac{1}{2}m\dot{r}^{2}+\frac{1}{2}mr^{2}\dot{\theta}^{2}+\frac{GMm}{r}
$$
Then the generalised momenta are
$$
\begin{align}
p_{r}&=m\dot{r} \\
p_{\theta}&=mr^{2}\dot{\theta}
\end{align}
$$
and the generalised forces are
$$
\begin{align}
F_{r}&=mr\dot{\theta}^{2}-\frac{GMm}{r^{2}} \\
F_{\theta}&=0
 \end{align}
$$
So angular momentum is conserved and the equations of motion are
$$
\begin{align}
\ddot{r}&=r\dot{\theta}^{2}-\frac{GM}{r^{2}} \\
2mr\dot{r}\dot{\theta}+mr^{2}\ddot{\theta}\Rightarrow\quad 0&=2\dot{r}\dot{\theta}+r\ddot{\theta}
\end{align}
$$
## 6.
Treating the upwards vertical as positive $z,$ with the upper mass being denoted with a subscript 2,
$$
\mathcal{L}(z_{1},z_{2},\dot{z}_{1},\dot{z}_{2})=\frac{1}{2}m(\dot{z}_{1}^{2}+\dot{z}_{2}^{2})-mg(z_{1}+z_{2})-\frac{1}{2}k(z_{2}-z_{1}-l)^{2} 
$$
When the bottom mass is in contact with the floor, set $z_{1}=0.$ Therefore
$$
\mathcal{L}(z_{2},\dot{z}_{2})=\frac{1}{2}m\dot{z}_{2}^{2}-mgz_{2}-\frac{1}{2}k(z_{2}-l)^{2}
$$
Changing the coordinate system to be in terms of the system centre $z_{c}$ and mass separation $z_{s},$
$$
\mathcal{L}(z_{c},\dot{z}_{c},z_{p},\dot{z}_{p})=m\left( \dot{z}_{c}^{2}+\frac{\dot{z}_{s}^{2}}{4} \right)-2mgz_{c}-\frac{1}{2}k(z_{s}-l)^{2}
$$
Then the generalised momenta are
$$
\begin{align}
p_{c}&=2m\dot{z}_{c} \\
p_{s}&=\frac{1}{2}m\dot{z}_{s}
\end{align}
$$
which can be interpreted physically as $p_{c}$ being the linear momentum of the centre of mass and $p_{s}$ being the linear momentum of one mass relative to the other.

The equation of motion is
$$
\frac{m}{2}\begin{bmatrix}
4\ddot{z}_{c} \\
\ddot{z}_{s}
\end{bmatrix}=-\begin{bmatrix}
2mg \\
k(z_{s}-l)
\end{bmatrix}
$$
which simplifies to
$$
\begin{bmatrix}
\ddot{z}_{c} \\
\ddot{z}_{s}
\end{bmatrix}
=-\begin{bmatrix}
g \\
\frac{2k}{m}(z_{s}-l)
\end{bmatrix}
$$
Solving this leads to
$$
\begin{bmatrix}
z_{c} \\
z_{s}
\end{bmatrix}=\begin{bmatrix}
z_{c,0}+\dot{z}_{c,0}t+\frac{1}{2}gt^{2} \\
A\sin\left( \sqrt{ \frac{2k}{m} }t+\phi \right)+l
\end{bmatrix}
$$
For some $A$ and $\phi.$ The centre of mass of the spring falls under the influence of gravity while the masses separation oscillates with simple harmonic motion about the natural spring length $l.$

## 7.
### Double pendulum of point masses

To find the Lagrangian for a double pendulum of two point masses of mass $m$ connected by light rods of length $l,$ first consider the motion of the centre of mass.
$$
\begin{align}
\mathbf{r}_{g}&= l\mathbf{e}_{r}+\frac{l}{2}\mathbf{e}_{\rho} \\
\mathrm{d}\mathbf{r}_{g}&=l\mathrm{d}\alpha \mathbf{e}_{\alpha}+\frac{l}{2}\mathrm{d}\beta \mathbf{e}_{\beta}

\end{align}
$$
Then the second fundamental form is
$$

\begin{align}

{\mathrm{d}\mathbf{r}}^{2}_{g}&=l^{2}{\mathrm{d}\alpha}^{2}+\frac{l^{2}}{4}{\mathrm{d}\beta}^{2}+\frac{l^{2}}{2}\mathrm{d}\alpha\mathrm{d}\beta \mathbf{e}_{\alpha}\cdot \mathbf{e}_{\beta} \\

&=l^{2}{\mathrm{d}\alpha}^{2}+\frac{l^{2}}{4}{\mathrm{d}\beta}^{2}+\frac{l^{2}}{2}\mathrm{d}\alpha\mathrm{d}\beta \cos(\alpha-\beta)
\end{align}

$$
Then the kinetic energy of the centre of mass is
$$

\begin{align}

T_{g}&=\frac{1}{2}m_{g} \frac{{\mathrm{d}\mathbf{r}}^{2}_{g}}{{\mathrm{d}t}^{2}} \\

&=m\left[ l^{2}\dot{\alpha}^{2}+\frac{l^{2}}{4}\dot{\beta}^{2}+ \frac{l^{2}}{2}\dot{\alpha}\dot{\beta}\cos(\alpha-\beta) \right]

\end{align}

$$
The rotational kinetic energy about the centre of mass is
$$

T_{\theta,g}=\frac{1}{2}ml^{2}\dot{\beta}^{2}

$$
Then the net kinetic energy is
$$

T=\frac{1}{2}ml^{2}\left[2\dot{\alpha}^{2} +\dot{\beta}^{2}+\dot{\alpha}\dot{\beta}\cos(\alpha-\beta)\right]

$$
and the potential energy is
$$
V=-mgl(2\cos\alpha+\cos\beta)
$$
### Double pendulum of uniform rods

Similarly, the motion of the centre of mass of the secondary rod again has the kinetic energy
$$
\begin{align}
T_{2,g}&=\frac{1}{2}m_{g} \frac{{\mathrm{d}\mathbf{r}}^{2}_{g}}{{\mathrm{d}t}^{2}} \\
&=\frac{1}{2}ml^{2}\left[ \dot{\alpha}^{2}+\frac{1}{4}\dot{\beta}^{2}+ \frac{1}{2}\dot{\alpha}\dot{\beta}\cos(\alpha-\beta) \right]
\end{align}
$$
With self-rotational $\mathrm{KE}$ of
$$
T_{2,\theta}=\frac{1}{2} \frac{ml^{2}}{12}\dot{\beta}^{2}
$$
The primary rod has $\mathrm{KE}$ 
$$
T_{1}=\frac{1}{2} \frac{ml^{2}}{3}\dot{\alpha}^{2}
$$
Hence the net $\mathrm{KE}$ is
$$
T=\frac{1}{2}ml^{2}\left[ \frac{4}{3}\dot{\alpha}^{2}+\frac{1}{3}\dot{\beta}^{2} +\frac{1}{2}\dot{\alpha}\dot{\beta}\cos(\alpha-\beta)\right] 
$$
and the potential energy is
$$
-\frac{l}{2}mg(3\cos\alpha+\cos\beta)
$$
tbc equations of motion, equilibrium states, condition for lower rod not flipping.

## 8.
$$
\mathcal{L}=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2})-mgh(x)
$$
Therefore the equations of motion are
$$
\begin{bmatrix}
m\ddot{x} \\
m\ddot{y}
\end{bmatrix}=\begin{bmatrix}
-mgh' \\
0
\end{bmatrix}
$$
$y$-momentum is conserved hence the motion can be classified via the total $x$ kinetic energy,
$$
E=\frac{1}{2}m\dot{x}^{2}+V(x)
$$
tbc

Conserving $y$-momentum, 
$$
\begin{align}
v_{i}\sin\theta_{i}&=v_{f}\sin\theta_{f} \\
v_{i}^{2}+2g\Delta h&=v_{f}^{2}
 \end{align}
$$
Combining these gives
$$
\frac{\sin\theta_{i}}{\sin\theta_{f}}=\sqrt{ 1+\frac{2gh}{v^{2}} }
$$
Even if we don’t neglect vertical kinetic energy, the system is still $y$-invariant. The full Lagrangian would be
$$
\mathcal{L}=\frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+h'(x)^{2}\dot{x}^{2})-mgh(x)
$$
which is equivalent for $h'(x)\ll 1.$

## 9.
$$
V_{\mathrm{eff}}=-\frac{g}{a}\cos\theta-\frac{1}{2}\omega^{2}\sin ^{2}\theta
$$
From the lectures,
$$
\mathcal{L}=\frac{1}{2}ma^{2}(\dot{\theta}^{2}+\omega^{2}\sin ^{2}\theta)+mga\cos\theta
$$
So the equation of motion is
$$
\begin{align}
\ddot{\theta}&=-\frac{g}{a}\sin\theta+\omega^{2}\sin\theta \cos\theta \\
&=-V'_{\mathrm{eff}}
 \end{align}
$$
with the given effective potential.

For equilibrium, we require
$$
V'_{\mathrm{eff}}=\frac{g}{a}\sin\theta-\omega^{2}\sin\theta \cos\theta=0
$$
This has roots at $\theta=0,\pi$ and
$$
\theta=\arccos\left( \frac{g}{a\omega^{2}} \right)
$$
if $\omega^{2} >\frac{g}{a}.$ To quickly test if $\theta=0$ is stable, linearise the equation of motion around that point to get
$$
\ddot{\theta}=\left( \omega^{2}-\frac{g}{a} \right)\theta
$$
which changes from $\mathrm{SHM}$ to exponential growth when $\omega^{2}> \frac{g}{a}.$
