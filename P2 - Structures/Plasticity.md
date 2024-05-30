## General methodology
1. Evaluate the ideal plastic collapse load for each possible plastic collapse mechanism
2. Identify the collapse mechanism that minimises the plastic collapse load

### Assumptions


## Upper-bound theorem
Any estimate for the plastic collapse load for a compatible mechanism by equating work done by the load and the plastic energy dissipation will be greater or equal to the actual collapse load.

Of the three basic principle of structural analysis (compatibility, material laws, equilibrium), this only uses two:
- compatibility 
- a material law

## Lower bound theorem
If a set of internal stress can be found in the structure that are in equilibrium with an applied load $W_{e}$ and nowhere violate the yield condition, then the applied load will be less than or equal to the actual collapse load $W_{c}$
$$
W_{e}\leq W_{c}
$$
This allows us to skip complicated considerations of which plastic hinges form where first before collapse.

This theorem provides a justification for elastic design. Any elastic solution is also a compatible equilibrium! Although it is unlikely to be the optimum theorem in plastic collapse, it is easily simulated.
### Propped cantilever example
#### The long way round…
Consider a propped cantilever.
![[propped-cantilever.png]]
Assuming a simplified elastic-plastic relationship,
![[e-p-rel.png]]
Considering one particular equilibrium solution with no self-stress,
![[parti-soln-propped-canti.png]]
And a state of self-stress with zero applied load,
![[self-stress-propped-canti.png]]
By compatibility we can find $M$ in the self-stress state.

>Note that at least two plastic hinges are required for collapse in this case.

Assuming the first plastic hinge forms at the root of the cantilever (where $M$ is highest), the bending moment at the plastic hinge is $M=M_{p}$ so we can solve the rest of the beam to find the location and collapse load for the 2nd plastic hinge where $|M(x)|=M_{p}$


## Interaction diagram
It is common to plot a the linear system of normalised applied moments $\left[ \frac{Hx}{M_{p}}, \frac{Vx}{M_{p}} \right]$ to identify which combinations of forces $[H, V]$ cause which failure modes.

![[interaction-diag.png]]
