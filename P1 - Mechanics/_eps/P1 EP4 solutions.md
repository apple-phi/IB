## 1.
$$
\begin{align}
\mathcal{L}(\mathbf{x},\dot{\mathbf{x}})&=\frac{1}{2}m\dot{\mathbf{x}}^{2}-\frac{1}{2}k\mathbf{x}^{2}-\frac{1}{2}K(x_{2}-x_{1})^{2} \\
&=\frac{1}{2}m\dot{\mathbf{x}}^{2}- \frac{1}{2}(k+K)\mathbf{x}^{2}+Kx_{1}x_{2} \\
\mathbf{p}=\frac{\partial \mathcal{L}}{\partial  \dot{\mathbf{x}}}&=m\dot{\mathbf{x}} \\
\mathbf{F}=\frac{\partial \mathcal{L}}{\partial \mathbf{x}}&=-(k+K)\mathbf{x}+K\begin{bmatrix}
x_{2} \\
x_{1} 
\end{bmatrix} \\
&=-(k+K)I\mathbf{x}+KP\mathbf{x} \\
&=-\begin{bmatrix}
k+K & -K \\
-K & k+K
\end{bmatrix}\mathbf{x} \\
&=-\kappa \mathbf{x}
 \end{align}
$$
where $P$ is the $2\times2$ permutation matrix. Hence the mass matrix is $M=mI.$ 

Then the Euler-Lagrange equations are
$$
M\ddot{\mathbf{x}}+\kappa \mathbf{x}=0
$$
which for steady harmonic oscillation becomes
$$
[\kappa-\omega^{2}M]\mathbf{x}=0
$$
Or, in this case we can write it as
$$
\kappa \mathbf{x}=\omega^{2}m\mathbf{x}
$$
and solve the eigenvalue problem for $\kappa$.
$$
\begin{align}
\det \kappa&=k^{2}+2K=\lambda_{1}\lambda_{2} \\
\operatorname{Tr}\kappa&=2k+2K=\lambda_{1}+\lambda_{2}
\end{align}
$$
Hence the mode frequencies are
$$
\begin{align}
\omega^{2}&=\frac{k}{m}, \frac{k+2K}{m} \\
 \end{align}
$$
with oscillation amplitudes
$$
\mathbf{x}=\begin{bmatrix}
1 \\
1
\end{bmatrix}, \begin{bmatrix}
1 \\
-1
\end{bmatrix}
$$
## 2.
Treating the pivot as the gravitational datum such that $h=-(l+x)\cos\theta,$
$$
\mathcal{L}(x,\dot{x},\theta,\dot{\theta})=\frac{1}{2}m\dot{x}^{2}+ \frac{1}{2}m(l+x)^{2}\dot{\theta}^{2}-\frac{1}{2}kx^{2}+mg(l+x)\cos\theta
$$
Then the equations of motion are
$$
m\begin{bmatrix}
\ddot{x} \\
(l+x)^{2}\ddot{\theta}
\end{bmatrix}+\begin{bmatrix}
kx-mg\cos \theta+m(l+x)\dot{\theta}^{2} \\
mg(l+x)\sin\theta + 2m(l+x)\dot{x}\dot{\theta}
\end{bmatrix}
=0
$$
A stable equilibrium requires $\nabla V=\mathbf{F}=0$ and $\nabla^{2}V>0.$ Hence $(x_{0},\theta_{0})=\left( \frac{mg}{k},0 \right).$

Linearising the equations of motion around this point gives
$$
m\begin{bmatrix}
\ddot{x} \\
\left( l+x_{0} \right)^{2}\ddot{\theta}
\end{bmatrix}+\begin{bmatrix}
kx \\
mg(l+x_{0})\theta
\end{bmatrix}=0
$$
while linearising the Lagrangian gives
$$
\mathcal{L}=\frac{1}{2}m\dot{x}^{2}+\frac{1}{2}m(l+x_{0})^{2}\dot{\theta}^{2}-\frac{1}{2}kx^{2}+mg(l+x_{0})\cos\theta
$$
so the mass and stiffness matrices are
$$
\begin{align}
M&= m\operatorname{diag}[1,(l+x_{0})^{2}] \\
K&=\operatorname{diag}[k,mg(l+x_{0})]
\end{align}
$$
From the linearised equations of motions we can see that
$$
\omega^{2}=\frac{k}{m}, \frac{g}{l+x_{0}}
$$

## 3.
$$
\begin{align}
\mathcal{L}(\alpha,\beta,\dot{\alpha},\dot{\beta})&=\frac{1}{2}\left[ A\dot{\alpha}^{2}+B\dot{\beta}^{2}+2C\dot{\alpha}\dot{\beta}\cos(\alpha-\beta) \right] +D\cos\alpha+E\cos\beta \\
&\approx\frac{1}{2}\left[ A\dot{\alpha}^{2}+B\dot{\beta}^{2}+2C\dot{\alpha}\dot{\beta} \right] +D\left( 1-\frac{\alpha^{2}}{2} \right)+E\left( 1-\frac{\beta^{2}}{2} \right) \\
\end{align}
$$
Hence the equations of motion are
$$
\begin{bmatrix}
A\ddot{\alpha}+C\ddot{\beta} \\
B\ddot{\beta}+C\ddot{\alpha}
\end{bmatrix}+\begin{bmatrix}
D\alpha \\
E\beta
\end{bmatrix}=0
$$
Hence the mass and stiffness matrices are
$$
\begin{align}
M&=\begin{bmatrix}
A & C \\
C & B
\end{bmatrix} \\
K&=\begin{bmatrix}
D & 0 \\
0 & E
\end{bmatrix}
\end{align}
$$
At steady state oscillation,
$$
\begin{align}
\det(\omega^{2}M-K)&=\begin{vmatrix}
\omega^{2}A-D  & \omega^{2}C \\
\omega^{2}C & \omega^{2}B-E
\end{vmatrix} \\
&=(\omega^{2}A-D)(\omega^{2}B-E)-\omega ^{4}C^{2} \\
&=(AB-C^{2})\omega ^{4}-(BD+AE)\omega^{2}+DE=0 \\
\Rightarrow\quad \omega^{2}&= \frac{AE+BD\pm \sqrt{ (AE+BD)^{2}-4(AB-C^{2})DE }  }{2(AB-C^{2})}
 \end{align}
$$
tbc lab related qs

## 4.
At equilibrium, 
$$
x_{1}^{*}=x_{2}^{*}=l
$$
In general, the Lagrangian is
$$
\begin{align}
\mathcal{L}(\mathbf{x},\dot{\mathbf{x}})&=\frac{1}{2}m\left( \frac{\dot{x}_{1}+\dot{x}_{2}}{2} \right)^{2}+\frac{1}{2} \frac{ml^{2}}{12} \left( \frac{\dot{x}_{1}-\dot{x}_{2}}{l} \right)^{2}-\frac{1}{2}k(x_{1}-l)^{2}-\frac{1}{2}k(x_{2}-l)^{2} \\
&=\frac{1}{8}m(\dot{\mathbf{x}}^{2}+2\dot{x}_{1}\dot{x}_{2})+\frac{1}{24}m(\dot{\mathbf{x}}^{2}-2\dot{x}_{1}\dot{x}_{2})-\frac{1}{2}k\mathbf{x}^{2}  \\
&=\frac{1}{6}m(\dot{\mathbf{x}}^{2}+\dot{x}_{1}\dot{x}_{2})-\frac{1}{2}k\mathbf{x}^{2}
\end{align}
$$
Then the equations of motion are
$$
\frac{1}{3}m\ddot{\mathbf{x}}+\frac{1}{6}m\begin{bmatrix}
\ddot{x}_{2} \\
\ddot{x}_{1}
\end{bmatrix}+k\mathbf{x}=0
$$
Hence the mass and stiffness matrices are
$$
\begin{align}
M&=\frac{m}{6}\begin{bmatrix}
2 & 1 \\
1 & 2
\end{bmatrix} \\
K&=kI
\end{align}
$$
Therefore at steady steady harmonic motion,
$$
\begin{align}
\det(\omega^{2}M-K)&=\begin{vmatrix}
2m\omega^{2}-6k & m\omega^{2} \\
m\omega^{2} & 2m\omega^{2}-6k
\end{vmatrix} \\
&=4m^{2}\omega ^{4}+36k^{2}-24m\omega^{2}k-m^{2}\omega^{4}=0 \\
\Rightarrow\quad u\triangleq\frac{m\omega^{2}}{k}&=2,6
 \end{align}
$$
To find the eigenmodes,
$$
\begin{bmatrix}
2u-6 & u \\
u & 2u-6
\end{bmatrix}\mathbf{x}=0
$$
For $u=2,$
$$
\begin{align}
\begin{bmatrix}
1 & -1 \\
-1 & 1
\end{bmatrix}\mathbf{x}&=0 \\
\Rightarrow\quad x_{1}&=x_{2}
 \end{align}
$$
For $u=6,$
$$
\begin{align}
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}\mathbf{x}&=0 \\
\Rightarrow\quad x_{1}&=-x_{2}
 \end{align}
$$
Now introduce two new parameters $h$ and $\theta$ based on these normal modes:
$$
\begin{align}
h&= \frac{x_{1}+x_{2}}{2} \\
\theta&= \frac{x_{1}-x_{2}}{2}
 \end{align}
$$
Now reformulating the Lagrangian in these parameters gives
$$
\begin{align}
\mathcal{L}(h,\theta,\dot{h},\dot{\theta})&=\frac{1}{2}m\dot{h}^{2}+\frac{1}{6}m\dot{\theta}^{2}-\frac{1}{2}k(h+\theta)^{2}-\frac{1}{2}k(h-\theta)^{2} \\
&= \frac{1}{2}m\dot{h}^{2}+\frac{1}{6}m\dot{\theta}^{2}-kh^{2}-k\theta^{2}
 \end{align}
$$
which is now separable in $h$ and $\theta.$ Physically, $h$ represents the height of the rod $\mathrm{COM}$ and $\theta$ represents the rod angle. 

## 5.
Let $\mathbf{q}=[\theta_{1},\theta_{2},\theta_{3}]^{\top},$ then
$$
\begin{align}
\mathcal{L}(\mathbf{q},\dot{\mathbf{q}})&=\frac{1}{2}I\dot{\mathbf{q}}^{2}-\frac{1}{2}k(\theta_{1}-\theta_{2})^{2}-\frac{1}{2}k(\theta_{2}-\theta_{3})^{2} \\
 \end{align}
$$
so the equations of motion are
$$
\begin{align}
I\ddot{\mathbf{q}} +k\begin{bmatrix}
\theta_{1}-\theta_{2} \\
-\theta_{1}+2\theta_{2}-\theta_{3} \\
-\theta_{2}+\theta_{3}
\end{bmatrix}=0
\end{align}
$$
Hence the mass and stiffness matrices are
$$
\begin{align}
M&=\operatorname{diag}(I,I,I) \\
K&=k\begin{bmatrix}
1 & -1 & 0 \\
-1 & 1 & -1 \\
0 & -1 & 1
\end{bmatrix}
\end{align}
$$
The mass matrix is a multiple of identity so the normal modes will be orthogonal. Hence the steady state oscillation frequencies are given when
$$
\begin{bmatrix}
I\omega^{2}-k & k & 0 \\
k & I\omega^{2}-k & k \\
0 & k & I\omega^{2}-k
\end{bmatrix}\mathbf{q}=0
$$
From this matrix we can see that one eigenvector is $\omega^{2}=\frac{k}{I}.$ This corresponds to the mode $\mathbf{q}_{1}=[1,0,-1]^{\top}.$ From intuition we can also see the translational mode at $\omega^{2}=0,$ $\mathbf{q}_{0}=[1,1,1]^{\top}$ 

Then we know the last mode is given by
$$
\mathbf{q}_{2}=\mathbf{q}_{1}\times \mathbf{q}_{0}=\begin{bmatrix}
1 \\
0 \\
-1
\end{bmatrix}\times\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix}
=\begin{bmatrix}
1 \\
-2 \\
1
\end{bmatrix}
$$
and from the matrix, this occurs at $\omega^{2}=\frac{3k}{I}.$

tbc step change in disk 1

We can write the motion as
$$
\dot{\mathbf{q}}=A\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix}+B\begin{bmatrix}
1 \\
0 \\
-1
\end{bmatrix}\cos\left( \omega_{1}t \right)+C\begin{bmatrix}
1 \\
-2 \\
1
\end{bmatrix}\cos\left( \omega_{2} t\right)
$$
and impose the initial condition $\mathbf{q}_{0}=[\omega+\Omega,\omega,\omega].$
$$
\begin{aligned}
&\begin{cases}
\begin{align}
A+B+C&=\omega+\Omega \\
A-2C&=\omega \\
A-B+C&=\omega
\end{align}
 \end{cases}
\\ \\
&\Rightarrow\quad \begin{bmatrix}
A \\
B \\
C
\end{bmatrix}=\begin{bmatrix}
\omega+\frac{\Omega}{3} \\
\frac{\Omega}{2} \\
\frac{\Omega}{6}
\end{bmatrix}
 \end{aligned}
$$
Hence the resulting motion is
$$
\begin{align}
\mathbf{q}&=\left( \omega+\frac{\Omega}{3} \right)\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix}t+\frac{\Omega}{2\omega_{1}}\begin{bmatrix}
1 \\
0 \\
-1
\end{bmatrix}\sin(\omega_{1}t)+\frac{\Omega}{6\omega_{2}}\begin{bmatrix}
1 \\
-2 \\
1
\end{bmatrix}\sin(\omega_{2}t)
 \end{align}
$$
So the twist angles are given by
$$
\begin{align}
\theta_{1}-\theta_{2}&=\left( \frac{\Omega}{2\omega_{1}}\sin(\omega_{1}t)+\frac{\Omega}{6\omega_{2}}\sin(\omega_{2}t) \right)-\left( -\frac{\omega}{3\omega_{2}}\sin(\omega_{2}t) \right) \\
&=\frac{\Omega}{2\omega_{1}}\sin(\omega_{1}t)+\frac{\Omega}{2\omega_{2}}\sin(\omega_{2}t) \\ \\
\theta_{2}-\theta_{3}&=-\frac{\Omega}{3\omega_{2}}\sin(\omega_{2}t)-\left(- \frac{\Omega}{2\omega_{1}}\sin\omega_{1}t+\frac{\Omega}{6\omega_{2}}\sin(\omega_{2}t) \right) \\
&=\frac{\Omega}{2\omega_{1}}\sin(\omega_{1}t)-\frac{\Omega}{2\omega_{2}}\sin(\omega_{2})t
\end{align}
$$
So the maximum twist angle for both twists is the same (as we expect by symmetry) as is
$$
\begin{align}
\max(\theta_{1}-\theta_{2})=\max(\theta_{2}-\theta_{3})&=\frac{\Omega}{2\omega_{1}}+\frac{\Omega}{2\omega_{2}} \\
&=\frac{\Omega}{2}\left( \sqrt{ \frac{I}{k} }+\sqrt{ \frac{I}{3k} } \right) \\
&=\frac{\Omega}{2}\sqrt{ \frac{I}{k} }\left( 1+\frac{1}{\sqrt{ 3 }} \right) 
 \end{align}
$$


## 6.
tbc Python

## 7.
The mass has inertial coordinate and velocity
$$
\begin{align}
\mathbf{r}&=\begin{bmatrix}
l\sin\theta \\
h-l\cos\theta
\end{bmatrix} \\
\dot{\mathbf{r}}&=\begin{bmatrix}
l\dot{\theta}\cos\theta \\
\dot{h}+l\dot{\theta}\sin\theta
\end{bmatrix}
 \end{align}
$$

So the Lagrangian is
$$
\begin{align}
\mathcal{L}(\theta,\dot{\theta}, t)&=\frac{1}{2}m\mathbf{r}^{2}-mg(h-l\cos\theta) \\
&=\frac{1}{2}(l^{2}\dot{\theta}^{2}+\dot{h}^{2}+2l\dot{h}\dot{\theta}\sin\theta)-gh+gl\cos\theta
 \end{align}
$$
Then the equation of motion is
$$
\begin{align}
0&=\frac{\mathrm{d} }{\mathrm{d}t} \{l^{2}\dot{\theta}+l\dot{h}\sin\theta\}-l\dot{h}\dot{\theta}\cos\theta+gl\sin\theta \\
&=l^{2}\ddot{\theta}+l\ddot{h}\sin\theta+l\dot{h}\dot{\theta}\cos\theta-l\dot{h}\dot{\theta}\cos\theta+gl\sin\theta \\
&=l^{2}\ddot{\theta}+l(g+\ddot{h})\sin\theta
 \end{align}
$$
So for small oscillations the time period is
$$
T=2\pi \sqrt{ \frac{l}{g+a} }
$$
The downward configuration will become a potential hill instead of a potential well at $a<-g.$

## 8.
$$
\begin{align}
\mathcal{L}(\mathbf{x},\dot{\mathbf{x}})&=\frac{1}{2}m\dot{\mathbf{x}}^{2}+Fx_{1}-\frac{1}{2}k\mathbf{x}^{2}-\frac{1}{2}k(x_{1}-x_{2})^{2} \\
&=\frac{1}{2}m\dot{\mathbf{x}}^{2}+F_{0}x_{1}\cos(\omega t)-k\mathbf{x}^{2}+kx_{1}x_{2} \\
 \end{align}
$$
So the equations of motion are
$$
\begin{align}
\begin{bmatrix}
F_{0} \\
0
\end{bmatrix}\cos(\omega t)&=m\ddot{\mathbf{x}}+2k\mathbf{x}-k\begin{bmatrix}
x_{2} \\
x_{1}
\end{bmatrix} \\
&=m\ddot{\mathbf{x}}+\underbrace{k \begin{bmatrix}
2 & -1 \\
-1 & 2
\end{bmatrix}}_{ \kappa }\mathbf{x}
 \end{align}
$$
At the steady state, let $\mathbf{x}(t)=\mathbf{a}\cos(\omega t)$ so
$$
[\kappa-m\omega^{2}I]\mathbf{a}=F_{0}\hat{\mathbf{x}}_{1}
$$
Hence the steady state oscillation amplitudes are
$$
\begin{align}
\mathbf{a}&=\begin{bmatrix}
2k-m\omega^{2}  & -k \\
-k  & 2k-m\omega^{2}
\end{bmatrix}^{-1}\begin{bmatrix}
F_{0} \\
0
\end{bmatrix} \\
&=\frac{F_{0}}{m(\omega^{2}-\omega_{1}^{2})(\omega^{2}-\omega_{2}^{2})}\begin{bmatrix}
2k-m\omega^{2} \\
k
\end{bmatrix}
 \end{align}
$$

## 9.
The kinetic energy is
$$
T=ml^{2}\dot{\theta}^{2}+ma^{2}(\dot{\theta}+\dot{\phi})^{2}
$$
while the potential energy is
$$
V=-2mgl\cos \theta
$$
hence the Lagrangian is
$$
\begin{align}
\mathcal{L}(\theta,\phi,\dot{\theta},\dot{\phi})&=ml^{2}\dot{\theta}^{2}+ma^{2}(\dot{\theta}+\dot{\phi})^{2}+2mgl\cos \theta \\
&\sim \frac{1}{2}l^{2}\dot{\theta}^{2}+\frac{1}{2}a^{2}(\dot{\theta}+\dot{\phi})^{2}+gl\cos \theta
 \end{align}
$$
so the equations of motion are
$$
\begin{bmatrix}
(l^{2}+a^{2})\ddot{\theta}+a^{2}\ddot{\phi} \\
a^{2}(\ddot{\theta}+\ddot{\phi})
\end{bmatrix}=-\begin{bmatrix}
gl\sin\theta \\
0
\end{bmatrix}
$$
So when $\phi=\phi_{0}+b\sin(\omega t)$ we have
$$
(l^{2}+a^{2})\ddot{\theta}+gl\sin\theta=ba^{2}\omega^{2}\sin(\omega t)
$$
which gives maximum $\theta$ at resonance when $\omega^{2}=\omega_{0}^{2}$
$$
\omega^{2}=\frac{gl}{l^{2}+a^{2}}
$$
> A pendulum with variable length string is a parametric oscillator where $\theta$ is maximised when the driving frequency is twice the natural frequency $\omega^{2}=2\omega_{0}^{2}.$
