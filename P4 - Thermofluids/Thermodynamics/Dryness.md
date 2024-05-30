## Dryness fraction
When studying the liquid-vapour [[PVT diagrams|two-phase]] region for working fluids it can be useful to define a *dryness fraction* —the fraction by mass of the dry gas phase.

Comparing the phases by specific volume $v$ and dryness fraction $x$,
$$
\begin{align}
V_{\mathrm{net}} & = m_{f}v_{f}+m_{g}v_{g} \\
 \\
\Rightarrow\quad v_{\mathrm{net}} & =\frac{m_{f}}{m}v_{f}+\frac{m_{g}}{m}v_{g} \\
 & =(1-x)v_{f}+xv_{g} \\
 & =v_{f}+(v_{g}-v_{f})x
\end{align}
$$
so the dryness fraction, $x$, represents a linear interpolation parameter between the specific volumes of the liquid and gas states.

It also acts as the linear interpolation parameter of the enthalpy states when comparing the liquid and gas states of a working fluid:
$$
\begin{align}
h_{\mathrm{net}} & =(1-x)h_{f}+xh_{g} \\
 & =h_{f}+(h_{g}-h_{f})x
\end{align}
$$
> Since we know that *dryness fraction* sets the values of two state functions, it sets the values of *all* state functions similarly (entropy, free energy, etc.).

## Humidity
The *specific humidity* of water is
$$
\omega= \frac{m_{\text{water vapour}}}{m_{\text{dry air}}}= \frac{\left( M_{r}\cdot p \right) _{\text{water vapour}}}{\left( M_{r}\cdot p \right)_{\text{dry air}}}
$$
where $p$ is the partial pressure.

The *relative humidity* of water is the amount of moisture present in the air relative to the maximum moisture-holding capacity at that temperature.
$$
\phi= \frac{n_{\text{water vapour}}}{n^{*}_{\text{water vapour}}}=\frac{p_{\text{water vapour}}}{p^{*}_{\text{water vapour}}}
$$
where $*$ represents the state when the air is saturated with water vapour at that temperature.