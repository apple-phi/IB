tbc: Lecture 7

Lecture 8 content:
## Power system faults
There are 400+ faults (due to weather, insulation failure, etc.) per annum in the UK.

There are many kinds of fault:
![[types-of-fault.png]]
But we will only consider the most severe type—type $e.$ This is reasonable to compute since this fault system is still balanced.

## Protection

Two categories of protective devices: 
- Circuit breakers (opens on-load)
- Isolators (opens off-load)

Their circuit symbols are a cross and dialogical line respectively.
![[circuit-breaker-isolator-symbols.png]]

A fault has the following typical sequence of events:
1. Fault occurs
2. Sensors detect
3. Circuit breaker opens
4. Circuit breaker re-closes
5. Circuit breaker re-opens (if fault not cleared)
6. Isolators open
![[circuit-breaker-diagram.png|200]]
Circuit breakers operation is as follows:
1. Separates metal contacts 
2. Causes arcs
3. AC current passes through zero
4. A blast of fluid (air, oil, $\mathrm{SF_{6}}$) removes ionisation products to prevent arc re-striking

The isolator in series with the circuit-breaker opens when the current has been interrupted.

### Desired properties of protection
- **Discrimination**—only isolates faulty part of system
- **Stability**—breaker stays closed when fault is outside the protected zone
- **Sensitivity**—ability to set current level at which beaker opens
- **Speed**—breaker opens quickly enough to prevent damage to generators, transformers etc.
- **Reliability**—breakers should not open when there is no fault (15 % of faults are spurious)
- **Back-up**—separate system in case primary protection fails.

## Fault analysis
We need to determine fault current levels to specifiy breaker $\mathrm{VA}$ ratings
$$
\text{VA rating}=\sqrt{ 3 }\left( VI \right)_\text{nominal} 
$$
### Assumptions
- All generations can be modelled as $\pu{ 1\angle 0 pu}$ EMF in series with synchronous reactance
- Transmission lines and transformers can be modelled as series inductive reactances
- The effect of loads connected to the network are negligible

The general method is to reduce the network to the simplest Thevenin equivalent to find $X_{F(\mathrm{pu})}$ and $I_{F(\mathrm{pu})}$

### Example

![[Lecture 8.pdf#page=4]]
