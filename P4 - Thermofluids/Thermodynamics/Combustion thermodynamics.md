Consider the [[Combustion chemistry|combustion]] of methane under excess oxygen ($\lambda>1$),
$$
\mathrm{CH_{4} + 2\lambda\left( O_{2} + \frac{79}{21}N_{2} \right)} \longrightarrow\mathrm{CO_{2}+2\,H_{2}O +  \lambda \cdot\frac{158}{79}N_{2} + 2(\lambda-1)\,O_{2} }
$$
We can model this process (1→2) in a combustion engine as follows:
![[h-T combustion.png]]
The resulting thermal energy of the products can be calculated using the standard heat of combustion (point 0 on the diagrams) as a reference datum.
![[combustion-thermodynamics.png]]
Linearly interpolating $c_{p}$ between temperatures as appropriate and assuming it will not change much during the reaction so [[Perfect gas relationships|perfect gas]] assumptions apply,
$$
%[Please add the Plimsoll symbol (circle with a horizontal line through it) · Issue #2200 · KaTeX/KaTeX · GitHub](https://github.com/KaTeX/KaTeX/issues/2200)%
\def\minuso{{\mathrlap{\mathchoice{\kern{0.145em}}{\kern{0.145em}}{\kern{0.145em}}{\kern{0.145em}}\circ}{-}}}

\begin{align}
\dot{Q}_{0\to2} & =\dot{Q}_{1\to 0}+\dot{Q}_{c} \\
(\dot{m}\Delta h_{0\to2})_{\mathrm{products}} & =(\dot{m}\Delta h_{1\to 0})_{\mathrm{reactants}}+\dot{m}_{f}\Delta H^\minuso_{c} \\
\left( \sum n_{i}\Delta \bar{h}_{0\to2} \right)_{\mathrm{products}} & =\left( \sum n_{i}\Delta \bar{h}_{1\to 0} \right)_{\mathrm{products}}+n_{f}\Delta \bar{H}^\minuso_{c}
\end{align}
$$
With known molar enthalpy values, this equation can be used to solve for the [[Combustion chemistry#Air-Fuel equivalence ratio ($ lambda$)|equivalence ratio]].

>Note that $\Delta H^\minuso_{c}<0$ because combustion is exothermic.
