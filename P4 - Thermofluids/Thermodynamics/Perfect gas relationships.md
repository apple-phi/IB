A perfect gas is an ideal gas that assumes constant heat capacities ($c_{p}$ and $c_{v}$):
$$
\begin{cases}
\begin{align}
\mathrm{d}u=c_{v}\mathrm{d} T\\
\mathrm{d} h=c_{p}\mathrm{d} T
\end{align}
\end{cases}
$$
## Change in specific entropy
Applying these assumptions to the [[Laws of Thermodynamics]] per unit mass:
$$
\mathrm{d}s =
\begin{cases}
\begin{align}
\frac{ c_{v}\mathrm{d}T}{T} & +\frac{p\mathrm{d}v}{T} \\
 \frac{c_{p}\mathrm{d}T}{T} & -\frac{v\mathrm{d}p}{T}
\end{align}
\end{cases}
$$
so integrating and using the ideal gas equation $R=\frac{pv}{T}$gives:
$$
\begin{aligned}
\Delta s&=\begin{cases}
\begin{aligned}
c_{v}\ln \frac{T_{2}}{T_{1}} & +R\ln \frac{v_{2}}{v_{1}} \\
c_{p}\ln \frac{T_{2}}{T_{1}} & -R\ln \frac{p_{2}}{p_{1}} \\
c_{v}\ln \frac{p_{2}}{p_{1}} & +c_{p}\ln \frac{v_{2}}{v_{1}} \\
\end{aligned}
\end{cases}\\
\\
&=\begin{cases}
\begin{align}
c_{v}\ln r_{T} &+R\ln r_{v} \\
c_{p}\ln r_{T} &-R\ln r_{p} \\
c_{v}\ln r_{p} &+c_{p}\ln r_{v}
\end{align}
\end{cases}
\end{aligned}
$$
## Isentropic changes
In the case when $\Delta s=0$, the above relationships can be expressed by exponentiating as
$$
\begin{aligned}\exp(\Delta S=0)=1=
&\begin{cases}
\begin{aligned}
{r_{T}}^{c_{v}} & \cdot {r_{v}}^{R} \\
{r_{T}}^{c_{p}} & \cdot {r_{p}}^{-R} \\
{r_{p}}^{c_{v}} & \cdot {r_{v}}^{c_{p}}
\end{aligned}
\end{cases}\\ \\
\Rightarrow\quad
&\begin{cases}
\begin{aligned}
{r_{T}}^{c_{v}} & = {r_{v}}^{-R} \\
{r_{T}}^{c_{p}} & = {r_{p}}^{R} \\
{r_{p}}^{c_{v}} & = {r_{v}}^{-c_{p}}
\end{aligned}
\end{cases}\\
\\
\Rightarrow\quad
&\begin{cases}
\begin{aligned}
T^{c_{v}} & = v^{-R} \\
T^{c_{p}} & = p^{R} \\
p^{c_{v}} & = v^{-c_{p}}
\end{aligned}
\end{cases}
\end{aligned}
$$
So using $\gamma= \frac{c_{p}}{c_{v}}$ and $c_{p}=c_{v}+R$,
$$
\begin{cases}
\begin{align}
pv^\gamma & =\mathrm{const.} \\
Tv^{\gamma-1} & =\mathrm{const.} \\
T & \propto p^{\frac{\gamma-1}{\gamma}}
\end{align}
\end{cases}
$$
where the proportionality constants are fractional combinations of the perfect gas constants $\{ c_{v}, c_{p}, R \}$.