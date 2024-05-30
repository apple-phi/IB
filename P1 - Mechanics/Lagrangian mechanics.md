Developed in 1788 by Giuseppe Luigi, comte de Lagrange, Lagrangian mechanics provides a standard way of deducing the equations of motion for complicated systems.

It becomes tricky for systems with non-conservative forces, and near-impossible for systems with non-holonomic contraints.
## Generalised coordinates
Given a system whose configuration is described by $n$ variables we can denote the degrees of freedom as
$$
\mathbf{q}=\{ q_{i} \}=q_{1},q_{2},q_{3},\dots, q_{n}
$$

## Lagrange’s equation
Define the Lagrangian as
$$
\begin{align}
\mathcal{L}&=T-V \\
&=T(\dot{q}_{i})-V(q_{i},t)
 \end{align}
$$
where $T=T(\dot{q}_{i})$ is the system kinetic energy and $V=V(q_{i},t)$ is the system potential energy.

>What follows is a slightly faulty proof (need to use calculus of variations to do it properly).

Since $T_{i}=\frac{1}{2}m_{i}\dot{q}_{i}^{2}$, the generalised momenta are
$$
\begin{align}
p_{i}&=\frac{\partial T}{\partial\dot{q}_{i}}  \\
&=\frac{\partial \mathcal{L}}{\partial\dot{q}_{i}} 
\end{align}
$$
By consideration of the work done to raise a potential $V_{i}=\int F_{i} \, \mathrm{d}q_{i}$ we can say the generalised forces are
$$
\begin{align}
F_{i}&=-\frac{\partial V}{\partial q_{i}}  \\
&=\frac{\partial \mathcal{L}}{\partial q_{i}}
 \end{align}
$$
Newton’s 2nd Law tells us that
$$
\begin{align}
\frac{\mathrm{d} p_{i}}{\mathrm{d}t}&=F_{i}  \\
\Rightarrow\quad \frac{\mathrm{d} }{\mathrm{d}t} \left( \frac{\partial \mathcal{L}}{\partial \dot{q}_{i}}  \right) &=\frac{\partial \mathcal{L}}{\partial q_{i}} 
\end{align}
$$
This is the Euler-Lagrange equation, aka. Lagrange’s equations of the 2nd kind.

>The Euler–Lagrange equation can only account for non-conservative forces _if_ a potential for those forces can be found.

## Noether’s theorem
If the Lagrangian is independent of the generalised coordinates $q_{i}$ then the generalised force is
$$
F_{i}=\frac{\partial \mathcal{L}}{\partial q_{i}} =0
$$
so the Euler-Lagrange equation becomes
$$
\frac{\mathrm{d} p_{i}}{\mathrm{d}t} =0
$$
This implies that momentum $p_{i}$ is constant and conserved. Therefore the generalised coordinate $q_{i}$ is termed to be *cyclic* or *ignorable*.

- Lagrangian invariance under translation implies conservation of momentum
- Lagrangian invariance under rotation implies conservation of angular momentum
- Lagrangian invariance under time $t$ implies conservation of total energy $E=T+V$

If the system has a continuous symmetry property then there are corresponding quantities whose values are conserved in time.

## Hamilton’s principle

Given an action functional defined as
$$
S=\int _{t_{1}}^{t_{2}}\mathcal{L} \, \mathrm{d}t 
$$
Then the Lagrangian satisfies the principle of least action, that is
$$
\delta S=\int _{t_{1}}^{t_{2}}\delta\mathcal{L} \, \mathrm{d}t =0
$$
where $\delta \mathcal{L}$ is the *variation* of $\mathcal{L},$ i.e.
$$
\delta \mathcal{L}=\sum\limits_{i}\left(  \frac{\partial \mathcal{L}}{\partial \dot{q}_{i}}\delta \dot{q}_{i} + \frac{\partial \mathcal{L}}{\partial {q}_{i}}\delta q_{i}\right) 
$$
which is structurally similar to the total differential form of $\mathcal{L}.$

## Hamiltonian
The Hamiltonian of a system is defined as
$$
\mathcal{H}=\mathbf{\dot{q}}\cdot \frac{\partial \mathcal{L}}{\partial \dot{\mathbf{q}}} -\mathcal{L}
$$
This quantity is equivalent to the system energy for systems where the generalised coordinates are natural (have no time-dependence).

This value is invariant under natural coordinate transformations.

## Singular Lagrangians

tbc

## One degree of freedom systems
Consider a mechanism with a single degree of freedom, which will in most cases be of the form
$$
\mathcal{L}(q,\dot{q})=\frac{1}{2}m\dot{q}^{2}-V(q)
$$
Then the associated generalised momentum and force are
$$
\begin{align}
p&=\frac{\mathrm{d} \mathcal{L}}{\mathrm{d}\dot{q}} =m\dot{q} \\
F&=\frac{\mathrm{d} \mathcal{L}}{\mathrm{d}q} -V'(q)
\end{align}
$$
So the equation of motion is
$$
\frac{\mathrm{d} }{\mathrm{d}t} (m\dot{q})=m \ddot{q}=-V'(q)
$$
### 1st integral of 1 DOF systems

Energy conservation guarantees that the first integration $\ddot{q}\to \dot{q}$ can *always* be done analytically. The trick is to first multiply by $\dot{q}.$
$$
\begin{align}
m\ddot{q}\dot{q}+V'(q)\dot{q}&=0 \\
\Rightarrow\quad \frac{\mathrm{d} }{\mathrm{d}t} \left\{ \frac{1}{2}m\dot{q}^{2}+V(q) \right\} &=0 \\
\Rightarrow\quad \frac{1}{2}m\dot{q}^{2}+V(q)&=E
\end{align}
$$
### Graphical intuition
If you plot $(q, V)$ then the vertical displacement of $V(q)$ from $V=E$ gives the kinetic energy $T=\frac{1}{2}m\dot{q}^{2}.$

![[1-dof-lagrangian.png]]

### Equilibrium states
Equilibrium occurs at stationary points of $E$ when  $\mathrm{d}E=0,$ which requires
$$
\begin{align}
V'&=0 \\
\dot{q}&=0
\end{align}
$$

### Phase portraits
To build intuition about the system it is useful to plot $(q, \dot{q})$ for each value of $E.$ This produces non-intersecting contours of constant $E.$ 

>The plot is self-consistent—$q$ increases along the trajectory when $\dot{q}>0$ and decreases when $\dot{q}<0$

Equilibrium points are shown as points where $\dot{q}=0$ 

tbc

### Stability and instability

tbc

### 2nd integral of 1 DOF systems

We now have velocity as a function of position,
$$
\dot{q}=\sqrt{ \frac{2}{m}\left[ E-V(q) \right]  }
$$
The time between two states $q_{1},q_{2}$ is then given by
$$
t_{q_{1}\to q_{2}}=\int_{q_{1}}^{q_{2}} \sqrt{ \frac{m}{2[E-V(q)]} } \, \mathrm{d}q 
$$
We say this has been reduced to quadrature because the problem is now just an area-finding problem. This integral is not always possible analytically.

In the case of a simple pendulum, this integral is
$$
\begin{align}
t_{\theta_{1}\to \theta_{2}}&=\int_{\theta_{1}}^{\theta_{2}} \sqrt{ \frac{ml^{2}}{2E+2mgl\cos\theta} } \, \mathrm{d}\theta  \\
&= \sqrt{ \frac{l}{2g} }\int_{\theta_{1}}^{\theta_{2}} \frac{1}{\cos\theta-\cos\theta_{1}}\,\mathrm{d}\theta
 \end{align}
$$
Then the time period of oscillation for an amplitude $\theta_{a}$ is
$$
T= 4\sqrt{ \frac{l}{2g} }\int_{0}^{\theta_{a}} \frac{1}{\cos\theta-\cos\theta_{a}}\,\mathrm{d}\theta
$$
By making the clever substitution $\sin u=\frac{\sin\left( \frac{\theta}{2} \right)}{\sin\left( \frac{\theta_{a}}{2} \right)},$ we can bring this into the standard form for the complete elliptic integral of the first kind, $K$.
$$
\begin{align}
T&=4\sqrt{ \frac{l}{g} } \int_{0}^{\frac{\pi}{2}} \frac{1}{\sqrt{ 1-\sin ^{2}\frac{\theta_{a}}{2}\sin ^{2}u }} \,\mathrm{d}u \\
&= \sqrt{ \frac{l}{g} }K\left( \sin \frac{\theta_{a}}{2} \right)
 \end{align}
$$
![[simple-pendulum-exact-soln.png]]

## Effective potential
From [[#Noether’s theorem]], in the case where the associated generalised momentum is constant $\dot{p}_{i}=0$ for a cyclic coordinate $q_{i},$ we name that constant as $k_{i}$ and substitute into the remaining equations of motion having eliminated one variable.

For example, for a conserved angular momentum $h=mr^{2}\dot{\theta},$ we can substitute $\dot{\theta}=\frac{h}{mr^{2}}$ to eliminate $\dot{\theta}.$

>These effective potentials can often be physically interpreted as a kinetic energy “barrier” term that varies with the generalised coordinates.

It is also often useful to linearise the effective potential near stationary points in the motion.

tbc: linearisation for $\mathrm{SHM}$ at potential wells

## Two body problem
Consider the free motion of two interacting particles. Their mutual interaction can be expressed in terms of their potential $V$
$$
\mathcal{L}(\mathbf{r}_{1},\mathbf{r}_{2},\dot{\mathbf{r}}_{1},\dot{\mathbf{r}}_{2})=\frac{1}{2}m_{1} |\dot{\mathbf{r}}_{1}|^{2}+\frac{1}{2}m_{1} |\dot{\mathbf{r}}_{2}|^{2}-V(|\mathbf{r}_{1}-\mathbf{r}_{2}|)
$$
Converting coordinates to be relative to the centre of mass,
$$
\mathcal{L}(\mathbf{r}_{g},\mathbf{r}_{s},\dot{\mathbf{r}}_{g},\dot{\mathbf{r}}_{s})
$$
tbc

## Stability and normal modes
The kinetic energy of an $n$-degree of freedom mechanism will be of the form
$$
\begin{align}
T(\mathbf{q},\dot{\mathbf{q}})&=\sum\limits_{ i,j }^{  } \frac{1}{2}M_{ij}(\mathbf{q})\dot{q}_{i}\dot{q}_{j} \\
&=\frac{1}{2}\dot{\mathbf{q}}^{\top}M(\mathbf{q})\dot{\mathbf{q}}
 \end{align}
$$
where $M(\mathbf{q})$ is a matrix of mass-like quantities, chosen to be symmetric (antisymmetric components have no contribution to $T$).

Hence the Lagrangian is
$$
\mathcal{L}(\mathbf{q},\dot{\mathbf{q}})=\frac{1}{2}\dot{\mathbf{q}}^{\top}M(\mathbf{q})\dot{\mathbf{q}}-V(\mathbf{q})
$$
Then the generalised force for coordinate $q_{k}$ is
$$
\begin{align}
F_{k}&=\frac{\partial \mathcal{L}}{\partial q_{k}}  \\
&=\frac{1}{2}\left( \dot{\mathbf{q}}^{\top}\frac{\partial M}{\partial q_{k}} \dot{\mathbf{q}} \right)_{k}-\frac{\partial V}{\partial q_{k}} 
 \end{align}
$$
Find an equilibrium point, which requires 
$$
\dot{\mathbf{q}}=\ddot{\mathbf{q}}=0
$$
This is satisfied by
$$
F_{k}=-\frac{\partial V}{\partial q_{k}}=0 
$$
Linearising the system in the neighbourhood of the stationary point $\mathbf{q}_{0},$ write
$$
\begin{align}
\mathbf{q}&=\mathbf{q}_{0}+\delta \mathbf{q} \\
\dot{\mathbf{q}}&=\delta  \dot{\mathbf{q}} \\
\ddot{\mathbf{q}}&=\delta  \ddot{\mathbf{q}}
\end{align}
$$
Therefore Taylor expansion of the Lagrangian gives
$$
\mathcal{L}(\mathbf{q},\dot{\mathbf{q}})\approx V(\mathbf{q}_{0})+\frac{1}{2}\dot{\mathbf{q}}^{\top}M\delta  \dot{\mathbf{q}}-\frac{1}{2} {\mathbf{q}}^{\top}K {\mathbf{q}}
$$
where $M$ and $K$ are constant symmetric matrices given by
$$
\begin{align}
M_{ij}&=\operatorname{Hess}_{\dot{q}}(T)=\left. \frac{ \partial^{2} T }{ \partial \dot{q}_{i} \partial \dot{q}_{j} } \right|_{\mathbf{q}=\mathbf{q}_{0}}  \\
K_{ij}&=\operatorname{Hess}(V)=\left. \frac{ \partial^{2} V }{ \partial {q}_{i} \partial q_{j} } \right|_{\mathbf{q}=\mathbf{q}_{0}}
\end{align}
$$
>Note that there are no linear terms in the expansion of $\mathcal{L}$ because $T$ is quadratic in $\dot{\mathbf{q}}$ and $V$ has no linear terms since it is nearby a stationary point.

Then the generalized momenta and forces are given by
$$
\begin{align}
\mathbf{p}&=\frac{\partial \mathcal{L}}{\partial  \dot{\mathbf{q}}}\approx M \dot{\mathbf{q}} \\
\mathbf{F}&=\frac{\partial \mathcal{L}}{\partial \mathbf{q}} \approx -K \mathbf{q}
\end{align}
$$
Therefore the full set of equations of motion can be written as
$$
M\ddot{\mathbf{q}}\approx-K\mathbf{q}
$$
Constant frequency mode solutions occur at solutions where the coordinates vibrate at $\omega,$
$$
\mathbf{q}=\mathbf{a}e^{ i\omega t }
$$
where $\mathbf{a}$ is a constant vector describing the “shape” of that particular oscillation mode. Hence this vector satisfies the generalized eigenvalue equation
$$
\omega^{2}M\mathbf{a}=K\mathbf{a}
$$

The resultant motion will be a linear superposition of the different mode shapes.

>A mode for which $\omega=0$ is termed to be translational.

The solution modes will be orthogonal if $M\propto I$ or $K\propto I.$ However, even if this is not the case, in general the following relationships hold:
$$
\begin{align}
\mathbf{a}^{\top}M\mathbf{a}&=0 \\
\mathbf{a}^{\top}K\mathbf{a}&=0
\end{align}
$$

## Computing Lagrangian dynamics
Lagrangian mechanics produces equations of motion of the form
$$
\ddot{\mathbf{q}}=f(\dot{\mathbf{q}},\mathbf{q})
$$
>Not much of this is examinable!

The examinable bits are:
- Forward Euler integration
- errors
- orders
- stability
- chaos

### Forward Euler integration
Consider the $\mathrm{ODE}$
$$
\frac{\mathrm{d} y}{\mathrm{d}t} =f(y,t)
$$
We can iteratively integrate as
$$
y_{n+1}=y_{n}+f_{n}\delta t+\mathcal{O}(\delta t^{2})
$$
To apply this to mechanics, consider the differential equations
$$
\begin{align}
\dot{x}&=v(t) \\
\dot{v}&=a(x,v,t)
\end{align}
$$
Then apply Forward Euler as
$$
\begin{align}
x_{n+1}&=x_{n}+v_{n}\delta t \\
v_{n+1}&=v_{n}+a_{n}\delta t
\end{align}
$$
This is an $\mathcal{O}(\delta t)$ solution. It also doesn’t conserve energy and hence the solution usually diverges.

### Backwards Euler
You can also do this the other way around by considering the *end* gradient / force,
$$
y_{n+1}=y_{n}+f_{n+1}\delta t+\mathcal{O}(\delta t^{2})
$$
which is applied to equations of motion as
$$
\begin{align}
x_{n+1}&=x_{n}+v_{n+1}\delta t \\
v_{n+1}&=v_{n}+a_{n+1}\delta t
\end{align}
$$
This is much more stable than Forwards Euler but is much more difficult to implement.

## Semi-implicit Euler (non-examinable)
We can balance the forwards and backwards Euler integrators to obtain a symplectic integrator. 
- Update the velocities using forwards Euler
- Updates the positions using backwards Euler
$$
\begin{align}
v_{n+1}&=v_{n}+a_{n}\delta t \\
x_{n+1}&=x_{n}+v_{n+1}\delta t \\
\end{align}
$$
This sequential method makes implementing the second, backwards Euler step much easier to implement.

### Leapfrog (non-examinable)
By interleaving the velocity and position calculations, we can write a 2nd order integrator as
$$
\begin{align}
x_{n+1}&=x_{n}+v_{n+\frac{1}{2}}\delta t \\
v_{n+\frac{3}{2}}&=v_{n+\frac{1}{2}}+a_{n+1}\delta t
\end{align}
$$
This provides much more stability and has an $\mathcal{O}(\delta t^{2})$ total error. 

>Note that this is algebraically equivalent to both Verlet and Velocity-Verlet integration.