## 1.
The forces due to rotation are much stronger than weight due to the high rotational speed. The acceleration at $A$ is
$$
\begin{align}
\mathbf{a}_{a}&=-R\Omega^{2}\mathbf{e}_{1}
 \end{align}
$$
And the relative acceleration of $B$ to $A$ is
$$
\mathbf{a}_{b / a}=2a\ddot{\theta}\mathbf{e}_{2}^{*}-2a(\dot{\theta}+\Omega)^{2}\mathbf{e}_{2}$$
Then the net acceleration of the midpoint of $AB$ is
$$
\mathbf{a}_{g}=-R\Omega^{2}\mathbf{e}_{1}+a\ddot{\theta}\mathbf{e}_{2}^{*}-a(\dot{\theta}+\Omega)^{2}\mathbf{e}_{2}
$$
Consider moments about $A$ on $AB.$ The only external forces on $AB$ can be exerted through $A,$ that is, any self-acceleration terms do *not* produce an additional torque on top of the torque exerted on $AB$ at $A$ by the hub. The torque $T$ is balanced by the inertia $I_{a}\ddot{\theta},$
$$
\begin{aligned}
&& I_{a}\ddot{\theta}&=T_{\mathrm{hub}} \\
&\Rightarrow&\frac{m(2a)^{2}}{3}\ddot{\theta}&=-mR\Omega^{2}|\mathbf{e}_{1}\times \mathbf{e}_{2}| \\
&\Rightarrow& \frac{4}{3}a\ddot{\theta}+R\Omega^{2}\sin\theta&=0 \\
&\Rightarrow& \ddot{\theta}+\frac{3}{4a}R\Omega^{2}\theta&=0 \\
&\Rightarrow& \omega&=\Omega\sqrt{ \frac{3R}{4a} }
\end{aligned}
$$
If the small-amplitude motion is $\theta=\theta_{0}\sin\omega t$ then 
$$
\begin{align}
\dot{\theta}&=\theta_{0}\omega \cos\omega t\\
\ddot{\theta}&=-\theta_{0}\omega^{2}\sin\omega t
 \end{align}
$$
By small angle approximations we can say that
$$
\begin{align}
\mathbf{e}_{1}&=(\mathbf{e}_{1}\cdot \mathbf{e}_{2})\mathbf{e}_{2}+(\mathbf{e}_{1}\cdot \mathbf{e}_{2}^{*})\mathbf{e}_{2}^{*} \\
&=\cos(\theta)\mathbf{e}_{2}-\sin(\theta) \mathbf{e}_{2}cnoj \\
&\approx\mathbf{e}_{2}-\theta \mathbf{e}_{2}^{*}
 \end{align}
$$
From the first part of the question, and assuming $\dot{\theta}\ll\Omega,$
$$
\begin{align}
\mathbf{a}_{g}&=-R\Omega^{2}\mathbf{e}_{1}+a\ddot{\theta}\mathbf{e}_{2}^{*}-a(\dot{\theta}+\Omega)^{2}\mathbf{e}_{2} \\
&\approx \left[ -a(\dot{\theta}+\Omega)^{2}-R\Omega^{2} \right] \mathbf{e}_{2}+(a\ddot{\theta}+R\Omega^{2}\theta)\mathbf{e}_{2}^{*} \\
&\approx-\Omega^{2}(a+R)\mathbf{e}_{2}+(-a\omega^{2}+R\Omega^{2})\theta \mathbf{e}_{2}^{*} \\
&=-\Omega^{2}(a+R)\mathbf{e}_{2}+\left( -\frac{3}{4}R\Omega^{2}+R\Omega^{2} \right)\theta \mathbf{e}_{2}^{*}  \\
&=-\Omega^{2}(a+R)\mathbf{e}_{2}+\frac{1}{4}R\Omega^{2}\theta_{0}\sin(\omega t)\mathbf{e}_{2}^{*} \\
 \\
\Rightarrow\quad \mathbf{R}_{a}&=m\mathbf{a}_{g}
 \end{align}
$$

## 2.
$B$ has angular accel. $\alpha$ so has linear accel. $l\alpha$ downwards on the page. The instantaneous centre of $CBD$ is at $C$ so $CBD$ rotates at angular velocity $2\alpha$ clockwise.
![[2P2 EP2 Q2.png]]
Conserving angular momentum,
$$
\begin{align} 
T&=\sum I\ddot{\theta}\\
&=\alpha I_{AB / a}+\alpha I_{CD / a} +(2\alpha+\alpha) I_{CD / g} \\
&=\frac{\alpha ml^{2}}{3}+\frac{\alpha ml^{2}}{12}+\alpha ml^{2}+\frac{3aml^{2}}{12} \\
&=\frac{5}{3}\alpha ml^{2}
 \end{align}
$$
Taking moments about $A,$
$$
\begin{align}
T-\frac{\sqrt{ 3 }}{2}F_{e} \frac{l}{2}&=\frac{l}{2}ma_{AB / g}+lma_{CD / g}+ 2\alpha I_{g} +I_{g}\\
\Rightarrow\quad \frac{5}{3}\alpha ml^{2}-\frac{\sqrt{ 3 }}{4}lF_{e}&=\frac{l}{2}m\alpha  \frac{l}{2}+l^{2}m\alpha + \frac{ml^{2}}{6}+\frac{ml^{2}}{12} \\ \\
\Rightarrow\quad F_{e}&=\frac{2\sqrt{ 3 }}{9}ml\alpha
 \end{align}
$$
## 3.
Let $\rho$ be the mass per unit length.
$$
\begin{align}
\dot{\omega}&=\frac{T}{I_{p}} \\
&=\frac{T}{\left( \frac{\rho l^{3}}{3} \right) } \\
&= \frac{3T}{\rho l^{3}}
 \end{align}
$$
Then the data-book gives that the vertical reaction is 
$$
\begin{align}
V_{p}&= M \frac{l}{2}\dot{\omega} \\
&=\frac{3 T}{2l}
 \end{align}
$$
Shear force density is linear so shear force is quadratic. Fitting the terms gives that
$$
S(x)=V_{p}\left(\left( \frac{x}{l} \right)^{2}-1 \right)
$$
Then the bending moment is
$$
\begin{align}
M(x)&=V_{p}\left[ \frac{x^{3}}{3l^{2}}-x\right] +T
 \end{align}
$$
## 4.
By N2L,
$$
\begin{align}
\frac{b-a}{2}mg&=I_{p}\dot{\omega} \\
&= \frac{\dot{\omega}ml^{2}}{12}+\dot{\omega}m\left( \frac{b-a}{2} \right)^{2}\\
\Rightarrow\quad \dot{\omega}&= \frac{6(b-a)g}{l^{2}+3(b-a)^{2}} \\
&=\frac{6g(b-a)}{b^{2}+a^{2}+2ab+3b^{2}+3a^{2}-6ab} \\
&=\frac{3g}{2} \frac{b-a}{b^{2}+a^{2}-ab}
 \end{align}
$$
Consider a free section of the bar starting at a distance $x$ from $P.$ Resolving vertically, the shear force is
$$
S(x)=(b-x)\left( \frac{x+b}{2}\rho\dot{\omega}-\rho g \right)
$$
Max $M(x)$ occurs at $S=0$ so
$$
\begin{align}
x&= \frac{2g}{\dot{\omega}}-b\\
&=\frac{4}{3} \frac{b^{2}-a^{2}-ab}{b-a}-b
 \end{align}
$$
When $a> \frac{b}{2}$ the moments are entirely hogging in the longer part of the bar.

## 5.
$$
\begin{align}
\dot{\omega}&=\frac{T}{I_{p}}\\
&= \frac{T}{M(k^{2}+l^{2})}
 \end{align}
$$
The radial reaction is
$$
R_{\rho}=-M\omega^{2}l
$$
The perpendicular reaction is
$$
\begin{align}
R_{\theta}&=Ml\dot{\omega} \\
&=\frac{Tl}{k^{2}+l^{2}}
 \end{align}
$$
Cut from $A$ to the free end. Because the bar is light, the shear force is the same as the perpendicular reaction force, $S=-R_{\theta}$. Hence the moment distribution is
$$
\begin{align}
\mathcal{M}(x=l-a)&=\int M\omega^{2}l \, \mathrm{d}x  \\
&=T-\frac{Tlx}{k^{2}+l^{2}}
 \end{align}
$$
## 6.
$$
\begin{align}
\dot{\omega}&=\frac{mga\cos\theta}{\left( \frac{m(2a)^{2}}{3} \right)} \\
&= \frac{3g}{4a}\cos\theta
 \end{align}
$$
Take a cut from $r=x$ to the free end. Then consider perpendicular equilibrium.
$$
S(x)=\rho(2a-x)\left( \frac{x+2a}{2}\dot{\omega}-\frac{g\sqrt{ 2 }}{2} \right)
$$
Maximum bending moment when $S=0$ so
$$
\begin{align}
(x+2a)\dot{\omega}&=2g\cos\theta \\
\Rightarrow\quad (x+2a) \frac{3g}{4a}\cos\theta&=2g\cos\theta \\
\Rightarrow\quad x&=\frac{2}{3}a
 \end{align}
$$
## 7.
$$
\begin{align}
\boldsymbol{\omega}_{1}&=\frac{v}{R}\mathbf{k} \\
\boldsymbol{\omega}_{2}&=\boldsymbol{\omega}_{1}-\frac{v}{R}\mathbf{e}_{\theta} \\
&=\frac{v}{R}\mathbf{k}-\frac{v}{R}\mathbf{e}_{\theta}
\end{align}
$$
$$
\begin{align}
\mathbf{r}_{p}&=R\mathbf{e}_{1}+r\mathbf{e}_{2} \\
\dot{\mathbf{r}}_{p}&=R\boldsymbol{\omega}_{1}\times \mathbf{e}_{1}+r\boldsymbol{\omega}_{2}\times \mathbf{e}_{2} \\
\ddot{\mathbf{r}}_{p}&=R \dot{\boldsymbol{\omega}}_{1}\times \mathbf{e}_{1}+r \dot{\boldsymbol{\omega}}_{2}\times \mathbf{e}_{2} \\&+R\boldsymbol{\omega}_{1}\times\boldsymbol{\omega}_{1}\times \mathbf{e}_{1}+r\boldsymbol{\omega}_{2}\times \boldsymbol{\omega}_{2}\times \mathbf{e}_{2} 
 \end{align}
$$
Then $\dot{\boldsymbol{\omega}_{1}}=0$ and $\dot{\boldsymbol{\omega}}_{2}=\frac{v^{2}}{Rr}\mathbf{e}_{1}\times \mathbf{k}$ so 
$$
\begin{align}
\ddot{\mathbf{r}}_{p}&=\frac{v^{2}}{R}\mathbf{i}+\frac{v^{2}}{r}\mathbf{j}
 \end{align}
$$
Also, $\dot{\mathbf{r}}_{p}=0$ as expected for no slip.

tbc

## 8.
![[P1 EP2 Q8.png]]
The [[3D kinematics#Gyroscopic mechanics|gyroscopic couple]] is $\mathbf{Q}=\boldsymbol{\Omega}\times J\boldsymbol{\omega}.$ This adds an additional inertia force to the bearings.

tbc
## 9.
Databook gives $J=\frac{1}{2}ma^{2}.$ By vertical equilibrium, $V_{p}=mg.$

Balancing the gyroscopic couple with the weight of the gyroscope gives
$$
\begin{align}
mgd&=\Omega \times J\omega \\
\Omega&= \frac{2dg}{a^{2}\omega}
 \end{align}
$$
The horizontal reaction is $H_{p}=m\Omega^{2}d.$ Taking moments about the inner base topple point,
$$
\begin{align}
mgr&=H_{p}h \\
&=\left( \frac{2dg}{\alpha^{2}\omega} \right)^{2}mdh \\
\omega&= \frac{2dg}{\alpha^{2}}\sqrt{ \frac{dh}{gr} }
 \end{align}
$$
