Consider an ideal reversible [[Simple steady flow devices|steady flow device]] which absorbs heat and passes it all through a [[Carnot efficiency|reversible heat engine]] to generate power while rejecting thermal power $\dot{Q}_{\mathrm{out}}$ to the environment. It also generates power directly from the flow, producing total power output $\dot{W}_{out}$.
![[reversible-steady-flow.png|400]]

The standard steady flow analysis gives
$$
\begin{aligned}
&\begin{cases}
\begin{align}
-\dot{Q}_{\mathrm{out}}+\dot{W}_{\mathrm{out}}  & = \dot{m}\Delta h \\
\dot{m}\Delta s & =\frac{-\dot{Q}_{\mathrm{out}}}{T_{\mathrm{env}}}+\cancel{\Delta\dot{S}}_{\text{irrev}}
\end{align}
\end{cases}\\
\\
\Rightarrow\quad &\dot{W}_{\mathrm{out}}=\dot{m} (\underbrace {\Delta h-T_{\mathrm{env}}\Delta s}_{\Delta b})
\end{aligned}

$$
where $\Delta b$ is the change in specific availability. We define the *specific availability* of a flow as
$$
b=h-T_{\mathrm{env}}s
$$
and it is sometimes useful to define a quantity relative to the *dead state* where $b=b_{\mathrm{env}}$. As shown above, in the dead state it is not possible to generate power from a steady flow.
$$
\Xi=b-b_{\mathrm{env}}
$$
This quantity is known as the *exergy*. Note that $\Delta \Xi=\Delta b$ so these quantities can often be interchangeable.

>Note the resemblance to the [[Spontaneous reactions#Gibbs free energy|Gibbs free energy]].

The power *unavailable* for work is the thermal power lost,
$$
\dot{Q}_{\mathrm{out}}=\dot{m}T_{\mathrm{env}}\Delta s=T_{\mathrm{env}}\Delta \dot{S}
$$
