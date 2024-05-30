## 1.
From first principles, given $m=\rho xy$ for a lamina:
$$
\begin{align}
mk^{2} & =\iiint r^{2} \, \mathrm{d}m  \\
 & =\iint  \rho y^{2}\, \mathrm{d}x\,\mathrm{d}y \\
 & =\int_{-\frac{b}{2}}^{+\frac{b}{2}} \rho y^{2}a  \,\mathrm{d}y \\
 & =\left[ \frac{\rho ay^{3}}{3} \right]^{+ \frac{b}{2}}_{-\frac{b}{2}} \\
 & =\frac{\rho ab^{3}}{12} \\
 & =\frac{mb^{2}}{12}  \\
 \\
\Rightarrow\quad k & = \frac{b}{\sqrt{ 12 }}
\end{align}
$$
Using the [[Kinematics in Two Dimensions#The perpendicular axis theorem|perpendicular axis theorem]],
$$
\begin{align}
I_{zz} & =I_{xx}+I_{yy} \\
 & = \frac{m(a^{2}+b^{2})}{12}
\end{align}
$$
Now, applying the [[Kinematics in Two Dimensions#The parallel axis theorem|parallel axis theorem]],
$$
\begin{align}
I_{a} & =I_{zz}+m\left( \frac{a}{2} \right)^{2}+m\left( \frac{b}{2} \right)^{2} \\
 & =\frac{m(a^{2}+b^{2})}{3}
\end{align}
$$
## 2.
A point mass has $I=mr^{2}$ so 
$$
I_{C}=\overbrace{ m(l-x)^{2}}^{ m_{\mathrm{A}} }+\overbrace{ 2mx^{2}}^{ m_{\mathrm{B}} }+\overbrace{ \frac{ml^{2}}{12}}^{ \mathrm{rod} }+\overbrace{ m\left( x- \frac{l}{2} \right)^{2}}^{ \parallel\text{-axis} }
$$
$I_{C}$ is minimised when $\mathrm{d}I_{C}=0$ so at the minimum:
$$
\begin{align}
\frac{ \mathrm{d}I_{C} }{ \mathrm{d}x }  & =-2m(l-x)+4mx +m(2x-l) \\
 & =(2+4+2)x+(-2-1)l\\\\
\Rightarrow\quad x & = \frac{3l}{8} \\
 \\
	I_{C,\min} & = \frac{37}{48}ml^{2}
\end{align}
$$
This is also the centre of mass of the assembly, which fits the intuition given by the parallel axis theorem because $$
I'=I_{G}+mr^{2}\geq I_{G}
$$so $I'$ is minimised at the centre of mass when $r=0$
## 3.
The instantaneous centre of $BC$ is $L\sqrt{ 2 }$ from $C$ in the direction $DC$![[Drawing 2024-01-24 16.41.53.excalidraw]]So we have
$$
\begin{align}
\dot{\theta}_{bc}L\sqrt{ 2 } & =\frac{\omega L}{3} \\
 \\
\Rightarrow\quad \dot{\theta}_{bc} & =\frac{\omega}{3\sqrt{ 2 }}
\end{align}
$$
Then $|\mathbf{v}_{b}|=L\dot{\theta}_{bc}$ so $\dot{\theta}_{ab}=\dot{\theta}_{bc}$ also because $A$ is also a centre of the motion of $B$. Conserving rotational power,
$$
\begin{align}
T_{a}\dot{\theta}_{ab} & = Tw \\
 \\
\Rightarrow\quad T_{a} & =3\sqrt{ 2 }T
\end{align}
$$
## 4.
Applying Newton’s Third Law,
$$
\begin{align}
\ddot{\theta} & =\frac{T}{I_{a}} \\
 & = \frac{-mg\cos\theta \cdot \frac{L}{2}}{\frac{mL^{2}}{3}} \\
 & =- \frac{3g}{2L}\sin\theta \\ \\
	\Rightarrow\quad \left. \ddot{\theta} \,\right|_{t=0} & = - \frac{3g}{2L}\\
\end{align}
$$
Applying the identity $\ddot{\theta} = \dot{\theta}\frac{\mathrm{d}\dot{\theta}}{\mathrm{d}\theta}$ gives
$$
\Rightarrow\quad \dot{\theta} =\sqrt{ \frac{3g}{L}\cos\theta }
$$
The maximum vertical force at $A$ will be when both the gravitational force and the magnitude vertical component of the centripetal force are maximised, hence $\theta=0$ and $\ddot{\theta}=0$. Then,
$$
\begin{align}
\max(V_{a}) & =m\left[g+\dot{\theta}^{2}r\right]_{t=0} \\
 & =m\left[ g+ \frac{3g}{L}\cdot \frac{L}{2} \right]  \\
 & =\frac{5mg}{2}
\end{align}
$$
The horizontal component of tension is
$$
\begin{align}
H_{a} & = m\dot{\theta}^{2}r\sin\theta -m\ddot{\theta}r\cos\theta\\
 & = m\left( \frac{3g}{L}\cdot \frac{L}{2} +\frac{3g}{2L}\cdot \frac{L}{2} \right )\cos\theta \sin \theta \\
 & = \frac{9mg}{8}\sin 2\theta
\end{align}
$$
The maximum horizontal force at $A$ will be when the horizontal component of tension is maximised, at $\theta=\pm 45^{\circ}$
 $$
\max(H_{a})= \frac{9mg}{8}
$$
## 5.
The system remains motionless when $T_{a}\leq mg$ which requires $M\leq 3m$. For both masses to be lifted, $T_{ab}\geq2mg$. In the limiting case $T_{ab}=2mg$ before $B$ moves, $a_A=g$ so the lower pulley moves up by $\frac{g}{2}$, which also corresponds to $a_{M}$. Hence,
$$
\begin{align}
Mg-2T_{ab}  & = \frac{Mg}{2} \\
 \\
\Rightarrow\quad M & =8m
\end{align}
$$
In the case $M=4m$, $B$ is stationary so $2a_{u}=a_{\ell}$. Considering the tensions in upper and lower moving weights,
$$
\begin{aligned}
\begin{cases}
\begin{align}
T_{\ell}-mg & =ma_{\ell} \\
Mg-2T_{\ell} & =Ma_{u}
\end{align}
\end{cases}&\\
\\
\Rightarrow\quad Mg-2mg&=2ma_{\ell}+\frac{a_{\ell}}{2}M
\\
a_{\ell}&= \left. \frac{M-2m}{2m+\frac{M}{2}}g \,\right|_{M=4m}\\
&=\frac{g}{2}
\end{aligned}
$$
## 6.
At the maxima and minima, the kinetic energy is $\frac{1}{2}mr^{2}\dot{\theta}^{2}$. The increase in KE towards the bottom corresponds to the release in GPE,
$$
\frac{1}{2}mv^{2}_{\mathrm{max}}-\frac{1}{2}mv^{2}_{\mathrm{min}}=mgh
$$
Conserving angular momentum $\hat{p}=vr$,
$$
v^{2}_{\mathrm{max}}-\left( \frac{v_{\mathrm{max}}h}{2h} \right)^{2}=2gh
$$
Hence we find that
$$
\begin{bmatrix}
v_{\mathrm{max}} \\
v_{\mathrm{min}}
\end{bmatrix}
=\sqrt{ \frac{2gh}{3} }\begin{bmatrix}
2 \\
1
\end{bmatrix}
$$
For a stationary orbit at height $h$, the normal wall force must be induced by equal weight and centrifugal forces. Hence,
$$
\begin{align}
mg & =\frac{mu^{2}}{h} \\
 \\
\Rightarrow\quad u & =\sqrt{ gh }
\end{align}
$$
where $u$ is the orbit velocity. Conserving linear momentum at the point of impact,
$$
\begin{align}
mv_{\mathrm{max}} & =(m+M)u \\
 \\
\Rightarrow\quad M & =\frac{ m\sqrt{ \frac{8gh}{3}}-m\sqrt{ gh }}{\sqrt{ gh }} \\
 & =m\left( \sqrt{ \frac{8}{3} }-1 \right)
\end{align}
$$
