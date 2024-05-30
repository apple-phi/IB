In reality the [[Carnot efficiency|Carnot cycle]] is impractical for power plants with water as the working fluid:
1. The compression step is in the two-phase region, but it is impossible to design a pump to handle two-phase flow
2. In heat addition, the temperature is limited by the temperature at the [[PVT diagrams|critical point]]
3. The expansion through the turbine is in the two-phase region so liquid droplets will erode the turbine blades

## Rankine cycle
This cycle solves the first two of the above problems:
- Compression occurs in a purely liquid phase
- Heat addition starts at a lower temperature
![[rankine-cycle.png|600]]
> The outlet temperature is very close to ambient, which compensates the efficiency a little for the low maximum temperature.

## Superheated Rankine cycle
This solves the final issue by reducing the amount of turbine operation in the two-phase region. It also gives a greater average heating temperature, which increases efficiency.
![[superheated-rankine-cycle.png|400]]

>However, there are manufacturing limitations for high temperatures—it is difficult to build a turbine that operates well under such conditions.

![[superheated-rankine-cycle-impl.png|400]]

## Further improvements
The primary ways to improve efficiency are:
- Increase temperature of heat supplied
- Decrease temperature of heat wasted

### Decrease outlet pressure
Lowering $p$ lowers $T$ so heat rejected at lower temperature.
![[lower-compressor-temp-rankine.png|400]]
### Increase boiler pressure
Increasing $p$ increases $T$ so heat supplied at higher temperature.
![[increase-boiler-pressure-rankine.png|400]]
### Reheat cycle
- Increases the [[Dryness|dryness fraction]] of the outlet
- Increases average temperature of heat supplied
![[ideal-reheat-cycle.png|400]]
>You can reheat multiple times, but to diminishing returns. It is not practical to reheat more than twice.

## Combination cycles
You can solve the problem of wasted outlet flow [[Availability balance|availability]] in [[Real gas turbines|gas turbines]] by passing the high temperature outlet flow through a [[HRSG|HRSG]] heat exchanger to supply heat to the boiler step of the Rankine cycle.

![[gas-vapour-cycle.png]]
![[gas-vapour-schematic.png]]