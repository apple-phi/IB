## 1.
Assuming separability as $\phi(r,\theta)=R(r)T(\theta),$ for Laplace’s equation $\nabla^{2}\phi=0,$
$$
\begin{aligned}
&&\frac{1}{r}\partial_{r} \left( r\partial_{r}\phi  \right) +\frac{1}{r^{2}}\partial^{2}_{\theta}\phi &=0 \\
&\Rightarrow& \frac{T}{r}\partial_{r}\left( r\partial_{r}R  \right)+\frac{R}{r^{2}}\partial^{2}_{\theta}T &=0 \\ \\
&\Rightarrow& \frac{r}{R}\frac{\partial }{\partial r} \left( r\frac{\mathrm{d} R}{\mathrm{d}r}  \right)  &=-\frac{1}{T}\frac{ \mathrm{d}^{2} T }{ {\mathrm{d} \theta}^{2} }
 \end{aligned}
$$
The LHS is a function of $r$ only while the RHS is a function of $\theta$ only so for equality they must be constant.

It is given that $\phi(1,\theta )=\sin\theta$ therefore we can choose any $T\propto \sin\theta$ by scaling. The boundary conditions for $R$ are then
$$
\begin{align}
R(1)&=1 \\
R(2)&=2
\end{align}
$$
And the aforementioned constant is
$$
-\frac{1}{T}\frac{ \mathrm{d}^{2} T }{ {\mathrm{d} \theta}^{2} }= -\frac{1}{\sin\theta}\frac{ \mathrm{d}^{2}\sin\theta }{ {\mathrm{d}\theta}^{2} }=1 
$$
As before,
$$
\begin{aligned}
&&\frac{r}{R}\partial_{r} \left( r\partial_{r}R  \right)&=1 \\ 
&\Rightarrow& \frac{r}{R}\left( r\partial_{r}^{2}R +\partial_{r}R\right)&=1  \\
&\Rightarrow& r^{2}\partial^{2}_{r}R+r\partial_{r}R-R&=0 
\end{aligned}
$$
Either employ Frobenius method, or, more easily, assume $R=Ar^{\alpha},$ therefore
$$
\begin{align}
r^{2}\partial^{2}_{r}(Ar^{\alpha})+r\partial_{r}(Ar^{\alpha})-(Ar^{\alpha})&=0  \\
\alpha(\alpha-1)r^{\alpha}+\alpha r^{\alpha}-r^{\alpha} &=0 \\
 \end{align}
$$
Then either $r=0$ or $\alpha^{2}=1.$ Therefore the general solution to the differential equation is
$$
R=Br+\frac{C}{r}
$$
Applying boundary conditions:
$$
\begin{align}
R(1)&=B+C =1\\
R(2)&=2B+\frac{C}{2}=2 \\
 \\
\Rightarrow\quad (B,C)&=(1,0)
\end{align}
$$
So the final solution to $\phi$ is
$$
\phi=r\sin\theta
$$
## 2.
Considering the Poisson equation $\nabla^{2}\phi=-\cos\left( \frac{\pi x}{2L} \right)$ subject to $\phi(\pm L,y)=0$ and $\phi(x,\pm d)=0,$ try the particular integral $\phi_{p}=-A\nabla^{2}\phi.$ Therefore,
$$
\begin{align}
-A\left( \frac{\pi }{2L} \right) ^{2}\cos\left( \frac{\pi x}{2L} \right)&=-\cos\left( \frac{\pi x}{2L} \right) \\
\Rightarrow\quad A&=\left( \frac{2L}{\pi} \right)^{2}
 \end{align}
$$
The complementary function satisfies Laplace’s equation $\nabla^{2}\phi_{0}=0.$ Since $\phi_{0}=\phi-\phi_{p},$ it has the boundary conditions that
$$
\begin{align}
\phi_{0}(\pm L,y)&=0 \\
\phi_{0}(x,\pm d)&=-A\cos\left( \frac{\pi x}{2L} \right)
 \end{align}
$$
Assume $\phi_{0}=X(x)Y(y)$ is separable. Then
$$
\begin{align}
Y\partial^{2}_{x}X+X\partial^{2}_{y}Y&=0 \\
\Rightarrow\quad \frac{1}{X}\partial^{2}_{x}X&=-\frac{1}{Y}\partial^{2}_{y}Y
 \end{align}
$$
The LHS and RHS are functions of only $x$ and $y$ respectively, therefore must be constant. Let this constant be $C$ then
$$
\begin{align}
\partial^{2}_{x}X-CX&=0 \\
\Rightarrow\quad X&=Ae^{\sqrt{ C }x}+Be^{ -\sqrt{ C } x}+\cancel{f(y)} \\ \\
\partial^{2}_{y}Y+CY&=0 \\
\Rightarrow\quad Y&=M\sin(\sqrt{ C }y)+N\cos(\sqrt{ C }y)+\cancel{g(x)} \\
 \end{align}
$$
Combining $X$ and $Y,$
$$
\phi_{0}=(e^{ \omega x }+Be^{ -\omega x })(M\sin(\omega y)+N\cos(\omega y))
$$
Applying the boundary condition $\phi_{0}(\pm L,y)=0,$ we can see that $B=-1$ so the equation reduces to
$$
\phi_{0}=P\cosh(\omega x)(e^{ i\omega y }+Qe^{ -i\omega y })
$$
Applying the second boundary condition that $\phi_{0}(x,\pm d)=-A\cos \frac{\pi x}{2L},$ it is clear that 
$$
\begin{align}
\omega&=\frac{i\pi}{2L} \\
P(e^{ \pm i\omega d }+Qe^{ \mp i\omega d })&=-A \\
\end{align}
$$
Applying a symmetry argument, $Q=-1$ so
$$
P=-\frac{A}{\cos(\omega d)}
$$
Finally,
$$
\begin{align}
\phi_{0}&=-\frac{A\cos\left( \frac{\pi x}{2L} \right)\cosh\left( \frac{\pi y}{2L} \right)}{\cosh\left( \frac{\pi d}{2L} \right)} \\
 \\
\Rightarrow\quad \phi&=\phi_{0}+\phi_{p} \\
&=\left( \frac{2L}{\pi} \right)^{2}\cos\left( \frac{\pi x}{2L} \right)\left( 1-\frac{{\cosh \left( \frac{\pi y}{2L} \right)}}{\cosh\left( \frac{\pi d}{2L} \right)} \right)
 \end{align}
$$

## 3.
Given $f=f(x,t)$ s.t. $\partial^{2}_{t}f=\partial^{2}_{x}f+2\omega\partial_{x}f$ subject to $f(0,t)=\sin\omega t$ and $\partial_{x}f(0,t)=0,$ find $f.$ We know immediately that $\partial^{2}_{t}f$ is a constant $C.$ Assume that $f$ is separable and $f=X(x)T(t)$
$$
\begin{align}
X\partial^{2}_{t}T&=T\partial^{2}_{x}X+2\omega T\partial_{x}X \\
\Rightarrow\quad \frac{1}{T}\partial^{2}_{t}T&=\frac{1}{X}(\partial^{2}_{x}X+2\omega\partial_{x}X) 
\end{align}
$$
We can freely choose $T=\sin\omega t$ (so the constant $\frac{1}{T}\partial^{2}_{t}T=-\omega^{2})$ and then find $X$ as
$$
\begin{align}
\partial^{2}_{x}X+2\omega\partial_{x}X+\omega^{2}X&=0 \\
(\partial_{x}+\omega)^{2}X&=0 \\
\Rightarrow\quad X&=e^{ -\omega x }(A+Bx)
 \end{align}
$$
Applying the boundary conditions, $X(0)=1$ and $X'(0)=0$ therefore
$$
\begin{align}
A&=1 \\
B-\omega A&=0 \quad\Rightarrow\quad B=\omega
\end{align}
$$
Hence the separable solution for $f$ is
$$
f=e^{-\omega x}(1+\omega x)\sin\omega t
$$

## 4.
Separating variables as $T=X(x)Y(y),$ to satisfy Laplace’s equation $\nabla^{2}T=0,$
$$
\begin{align}
Y\partial^{2}_{x}X+X\partial^{2}_{y}Y&=0 \\
\Rightarrow\quad \frac{1}{X}\partial^{2}_{x}X&=-\frac{1}{Y}\partial^{2}_{y}Y=C
 \end{align}
$$
for some constant $C.$ At boundaries $\mathrm{AB}$ ($y=0$) and $\mathrm{BC}$ ($x=1$) there is linear temperature variation so
$$
\begin{align}
\partial^{2}_{x}X(1)&=\partial^{2}_{y}Y(0)=0=C
\end{align}
$$
Then integrating twice both $\partial^{2}_{x}X=0$ and $\partial^{2}_{y}Y=0$ we have 
$$
\begin{align}
X&=\alpha x+\beta \\
Y&=\gamma y+\delta
\end{align}
$$
Hence the separable solution for $T$ is
$$
T=XY=a+bx+cy+dxy
$$
for some $a,b,c,d.$ With no heat flux through $\mathrm{AC},$ $\mathbf{q}$ must be parallel to the boundary and normal to the boundary normal. Therefore
$$
\begin{align}
0&=\mathbf{q}\times \begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix} \\
&=-\lambda\begin{bmatrix}
\partial_{x}T \\
\partial_{y}T \\
\partial_{z}T
\end{bmatrix}\times \begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix} \\
&=-\lambda(\partial_{x}T-\partial_{y}T) \\
 \\
\Rightarrow\quad \partial_{x}T&=\partial_{y}T
 \end{align}
$$
Applying this condition to $T$ along $\mathrm{AB},$
$$
\begin{align}
b+dy&=c+dx
\end{align}
$$
Considering $(x,y)=(0,0),$ we can see that $b=c.$ From the given points of $T$ we can also see that
$$
\begin{align}
T(0,0)&=a=\pu{ 300K } \\
T(1,0)&=a+b=\pu{ 400K } \\
T(1,1)&=a+2b+d=\pu{ 800K } \\
 \\
\Rightarrow\quad (a,b,c,d)&=(300,100,100,300)
 \end{align}
$$

## 5.

Assuming separability, $n=X(x)T(t),$ then for $\partial_{t}n=\alpha\partial^{2}_{x}n,$ we have
$$
\begin{align}
X\partial_{t}T&=\alpha T\partial^{2}_{x}X \\
\Rightarrow\quad \frac{1}{T}\partial_{t}T&=\frac{\alpha}{X}\partial^{2}_{x}X
 \end{align}
$$
The $\mathrm{LHS}$ and $\mathrm{RHS}$ are independent from each other and therefore must be constant $k$. From the initial distribution $n=n_{0}\cos\left( \frac{\pi x}{d} \right)$ we can set $X=\cos\left( \frac{\pi x}{d} \right)$ hence the constant is
$$
k=-\frac{\alpha \pi^{2}}{d^{2}}
$$
Then to solve for $T,$ while satisfying the initial condition $T(0)=n_{0},$
$$
\begin{align}
\partial_{t}T-kT&=0 \\
\Rightarrow\quad T&=n_{0}e^{ kt }
 \end{align}
$$
Therefore the separable solution for $n$ is
$$
n=n_{0}e^{  -\frac{\pi^{2}}{d^{2}}\alpha t }\cos\left( \frac{\pi x}{d} \right)
$$

## 6.
To solve $\partial^{2}_{t}p=c^{2}\partial^{2}_{x}p,$ assume separable $p=X(x)T(t)$ therefore
$$
\begin{align}
XT''&=c^{2}TX''\\
\Rightarrow\quad \frac{T''}{T}&=\frac{c^{2}X''}{X}
\end{align}
$$
The $\mathrm{LHS}$ and $\mathrm{RHS}$ are independent and therefore must be a constant $-k^{2}.$
$$
\begin{cases}
\begin{align}
T''+k^{2}T&=0 \\
c^{2}X''+k^{2}X&=0
\end{align}
 \end{cases}
$$
Let $x=0$ be the closed end and $x=L$ be the open end.
$$
\begin{align}
T&=A\sin(kt+\theta) \\
X&=B\cos\left( \frac{k}{c}x+\phi \right) \\
\end{align}
$$
From the boundary condition $\partial_{x}p(0,t)=0$ we know $\partial_{x}X(0)=0.$ From the boundary condition $p(L,t)=0$ we know $X(L)=0.$ Therefore $k=\frac{cn\pi}{2L}$ and $\phi=0.$ Hence
$$
\begin{align} \\
p=TX=A\sin\left( \frac{n\pi}{2L}ct+\theta \right)\cos\left( \frac{n\pi}{2L}x \right)
\end{align}
$$
Then, for resonation at frequency $f$ as the fundamental frequency $n=1,$
$$
\begin{align}
\frac{\pi c}{2L}&=2\pi f \\
\Rightarrow\quad L&=\frac{c}{4f}=\pu{ 329mm }
 \end{align}
 $$
 with a wavelength of $\lambda_{1}=4L.$ At the second natural frequency $f=\frac{c}{2L},$ the wavelength is $\lambda_{2}=2L.$

## 7.
Assume separable $Y=X(x)T(x)$ then
$$
\begin{align}
\rho AX\partial_{t}^{2}T+EIT\partial^{4}_{x}X&=0 \\
\Rightarrow\quad -\frac{\rho A}{T}\partial^{2}_{t}T&=\frac{EI}{X}\partial ^{4}_{x}X
 \end{align}
$$
The $\mathrm{LHS}$ and $\mathrm{RHS}$ are independent so must both be equal to a constant $EIk^{4}=\rho A\omega^{2}$ if equal. Therefore
$$
\begin{align}
\partial_{x} ^{4}X-k^{4}X&=0 \\
\partial^{2}_{t}T+\omega^{2}T&=0
\end{align}
$$
as expected.

## 8.
Define $\tau(y,t)=\frac{T_{0}-T}{\Delta T}.$ By dimensional analysis,
$$
\begin{align}
\tau&=f(t,y,\alpha) \\
&=g\left( \frac{y}{\sqrt{ \alpha t }} \right) \\
&=g(\eta)
\end{align}
$$
Therefore $\sqrt{ \alpha t }$ is a characteristic length scale. The heat equation $\partial_{t}T=\alpha\nabla^{2}T$ implies that
$$
\begin{aligned}
&&\partial_{t}\tau&=\alpha\partial^{2}_{y}\tau \\
&\Rightarrow & \partial_{\eta} \tau\partial_{t}\eta&=\alpha\partial_{y}(\partial_{\eta}\tau\partial_{y}\eta) \\
&\Rightarrow &-\frac{y}{2t\sqrt{ \alpha t }}\partial_{\eta}\tau&=\alpha\partial_{y}\left( \frac{1}{\sqrt{ \alpha t }}\partial_{\eta}\tau \right) \\
&\Rightarrow &-\frac{\eta}{2t}\partial_{\eta}\tau&=\frac{\alpha}{\sqrt{ \alpha t }^{2}}\partial^{2}_{\eta}\tau \\
&\Rightarrow & \partial^{2}_{\eta}\tau+\frac{\eta}{2}\partial_{\eta}\tau&=0 \\
&\Rightarrow & \partial_{\eta}\tau&=Ae^{ -\frac{\eta^{2}}{4} } \\
&\Rightarrow &\tau&=A\int_{0}^{\eta} e^{ -\frac{\eta^{2}}{4} } \, \mathrm{d}\eta +B
 \end{aligned}
$$
The boundary conditions for $T(y,t)$ are $T(0,t)=T_{0}-\Delta T$ and $T(\infty,t)\to\infty$ so for $\tau(\eta)$ they are $\tau(0)=1$ and $\tau(\infty)\to 0.$ Therefore
$$
\tau=1-\frac{1}{\sqrt{ \pi }}\int_{0}^{\eta} e^{ \frac{-\eta^{2}}{4} } \, \mathrm{d}\eta 
$$
by employing the identity
$$
\int_{0}^{\infty} e^{ -x^{2} } \, \mathrm{d}x =\frac{\sqrt{ \pi }}{2}
$$

## 9.
$$
\begin{align}
\mathbf{x}^{\top}\mathbf{x}&=\mathbf{x}\cdot \mathbf{x}=14 \\
\mathbf{x}\mathbf{x}^{\top}&=\mathbf{x}\otimes\mathbf{x}=\begin{bmatrix}
1  &  2  & 3 \\
2 & 4 &  6 \\
3 & 6 & 9
\end{bmatrix}
\end{align}
$$
where $\otimes$ is the *outer product*.

## 10.
By definition,
$$
\begin{bmatrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{bmatrix}\begin{bmatrix}
1 \\
0 \\
0
\end{bmatrix}=\begin{bmatrix}
a_{11} \\
a_{21} \\
a_{31}
\end{bmatrix}
$$
With $A$ denoted by its column vectors,
$$
\overbrace{ \begin{bmatrix}
\mathbf{a}_{1} & \mathbf{a}_{2} & \mathbf{a}_{3}
\end{bmatrix}}^{ A }\begin{bmatrix}
x \\
y \\
z
\end{bmatrix}=x\mathbf{a}_{1}+y\mathbf{a}_{2}+z\mathbf{a}_{3}
$$
For general rotation $\theta$ about the $y$-axis,
$$
Q=\begin{bmatrix}
\cos\theta & 0 &  -\sin\theta\\
0 & 1 & 0 &  \\
\sin\theta & 0 & \cos\theta
\end{bmatrix}
$$
In this case,
$$
\begin{bmatrix}
\cos\theta & 0 &  -\sin\theta\\
0 & 1 & 0 &  \\
\sin\theta & 0 & \cos\theta
\end{bmatrix}\begin{bmatrix}
\frac{1}{\sqrt{ 2 }} \\
2 \\
\frac{1}{\sqrt{ 2 }}
\end{bmatrix}=\begin{bmatrix}
-\frac{1}{2} \\
2 \\
\frac{\sqrt{ 3 }}{2}
\end{bmatrix}
$$
Therefore $\theta=\frac{5}{12}\pi.$ Hence we find $Q$ as
$$
Q=\begin{bmatrix}
\frac{\sqrt{ 6 }-\sqrt{ 2 }}{4} & 0 & -\frac{\sqrt{ 6 }+\sqrt{ 2 }}{4} \\
0 & 1 & 0 \\
\frac{\sqrt{ 6 }+\sqrt{ 2 }}{4} & 0 & \frac{\sqrt{ 6 }-\sqrt{ 2 }}{4}
\end{bmatrix}
$$

## 11.
$$
\begin{align}
AX&=\begin{bmatrix}
\mathbf{a}_{1}^{\top} \\
\mathbf{a}_{2}^{\top} \\
\mathbf{a}_{3}^{\top}
\end{bmatrix}\begin{bmatrix}
\mathbf{x}_{1} & \mathbf{x}_{2} & \mathbf{x}_{3}
\end{bmatrix} \\
&=\begin{bmatrix}
\mathbf{a}_{1}\cdot \mathbf{x}_{1} & \mathbf{a}_{1}\cdot \mathbf{x}_{2} & \mathbf{a}_{1}\cdot \mathbf{x}_{3} \\
\mathbf{a}_{2}\cdot \mathbf{x}_{1} & \mathbf{a}_{2}\cdot \mathbf{x}_{2} & \mathbf{a}_{2}\cdot \mathbf{x}_{3} \\
\mathbf{a}_{3}\cdot \mathbf{x}_{1} & \mathbf{a}_{3}\cdot \mathbf{x}_{2} & \mathbf{a}_{3}\cdot \mathbf{x}_{3} 
\end{bmatrix}
 \end{align}
$$
Then $b_{21}=\mathbf{a}_{2}\cdot \mathbf{x}_{1}.$ Since $C=B^{\top},$ $c_{21}=\mathbf{a}_{1}\cdot \mathbf{x}_{2}.$

## 12.
$$
\begin{align}
X&=\begin{bmatrix}
\mathbf{x}_{1} & \mathbf{x}_{2}
\end{bmatrix} \\
U&=\begin{bmatrix}
\mathbf{u}_{1} & \mathbf{u}_{2}
\end{bmatrix}
\end{align}
$$
By inspection, to obtain $X=UA$ subject to $\mathbf{x}_{1}=\alpha \mathbf{u}_{1}+\beta \mathbf{u}_{2}$ and $\mathbf{x}_{2}=\gamma \mathbf{u}_{1}+\delta \mathbf{u}_{2},$ we require
$$
A=\begin{bmatrix}
\alpha  & \gamma\\
\beta & \delta
\end{bmatrix}
$$
The permutation matrix $P$ for a $2\times2$ matrix is
$$
P=\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$
by inspection and consideration of $P=PI.$

For the matrix given by
$$
Y=\begin{bmatrix}
\mathbf{x}_{1}^{\top} \\
\mathbf{x}_{2}^{\top}
\end{bmatrix}=X^{\top}
$$
it’s relationship with $U$ and $A$ is therefore
$$
\begin{align}
Y&=(UA)^{\top} \\
&=A^{\top}U^{\top} \\
&=\begin{bmatrix}
\alpha &\beta \\
\gamma  & \delta
\end{bmatrix}\begin{bmatrix}
\mathbf{u}_{1}^{\top} \\
\mathbf{u}_{2}^{\top}
\end{bmatrix}
 \end{align}
$$
