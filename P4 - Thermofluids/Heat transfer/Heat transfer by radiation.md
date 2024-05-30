Heat can be transferred through a vacuum without a transport medium by electromagnetic waves. Indeed, it can be transferred through a medium colder than either body.

![[electromag-spec.png]]
Thermal radiation is primarily infrared.

## Black bodies
This is an idealised object defined as
- completely absorb all incident radiation
- emit the maximum energy possible at the given temperature

The maximum radiant exitance (energy flux) of a black body is given by the Stefan-Boltzmann Law
$$
E_{b}^{\circ}=\sigma T^{4}
$$
where $\sigma$ is the Stefan-Boltzmann constant.

This comes from the monochromatic emissive power of a black body $E_{b\lambda}$ given by
$$
E_{b\lambda}^{\circ}(\lambda)= \frac{c_{1}\lambda^{-5}}{e^{\frac{c_{2}}{\lambda T}}-1}
$$
for given constants $c_{1}$ and $c_{2},$ integrated over all wavelengths.

![[bb-rad-spec.png]]
Note that the peak moves to shorter wavelengths as temperature increases. This demonstrates why heated objects go from red to orange to yellow etc. Indeed
$$
\lambda_{\max}\propto \frac{1}{T}
$$
## Real surfaces

Real surfaces absorb and emit less than a black body. We define the emissivity of a real surface relative to that of a black body as 
$$
\begin{align}
\varepsilon_{\lambda}(\lambda)&= \frac{E_{\lambda}}{E_{b\lambda}^{\circ} }
 \end{align}
$$

The total emissivity is then given by
$$
\begin{align}
\varepsilon(T)&=\frac{E}{E^{\circ}_{b}} \\
&= \frac{\int_{0}^{\infty} E_{\lambda} \, \mathrm{d}\lambda }{\int_{0}^{\infty} E^{\circ}_{b\lambda} \, \mathrm{d}\lambda } \\
&=\frac{\int_{0}^{\infty} \varepsilon_{\lambda}E^{\circ}_{b\lambda} \, \mathrm{d}\lambda }{\sigma T^{4}}
 \end{align}
$$

>Interestingly, water has a very high emissivity and is close to being a black body—the limited vision range of our eyes give us a false impression of its overall properties!

For conventional materials,
$$
|\varepsilon|<1
$$

## Grey bodies
A grey body is a body where the monochromatic emissivity $\varepsilon_{\lambda}$ is constant and independent of wavelength.

### Absorption, transmission and reflection
When radiation strikes a surface, fractions of the energy divide as:
- Reflectivity $\rho$—the fraction reflected
- Absorptivity $\alpha$—the fraction absorbed
- Transmittivity $\tau$—the fraction transmitted.
$$
\rho+\alpha+\tau=1
$$
For opaque objects, $\tau \approx 0.$

Kinds of reflection:
- specular
- diffuse

### Kirchhoff's identity
Due to quantum processes, the absorptivity is the same as the emissivity!
$$
\varepsilon=\alpha
$$
### Radiation to and from a non-black body

Define:
- Irradiation $G$—the incident radiant flux
- Radiosity $J$—the emitted radiant flux

The radiosity is composed of the emittance due to temperature (radiant exitance) and additional reflected radiant flux.
$$
J=E+\rho G
$$
Assuming a linear, opaque material,
$$
J=\varepsilon E^{\circ}_{b}+(1-\varepsilon)G
$$
The net radiation flux transfer through the object is then
$$
\begin{align}
\dot{q}&=J-G \\ \\
\dot{Q}&=\varepsilon (E^{\circ}_{b}-G)A \\
&= \frac{\varepsilon(E_{b}^{\circ}-J)A}{1-\varepsilon}
 \end{align}
$$

This can be interpreted as one of two linear resistance equations with:
- current $\dot{Q}$
- potential difference $E^{\circ}_{b}-G$ or $E^{\circ}_{b}-J$
- surface resistance $\frac{1}{\varepsilon A}$ or $\frac{1-\varepsilon}{\varepsilon A}$

## Radiative exchange between surfaces
Consider two nearby surfaces emitted co-incident radiation. Let $f_{ij}$ be the fraction of energy that leaves $i$ which arrives at $j.$ The total radiative exchange is
$$
\begin{align}
\dot{Q}_{12}&=J_{1}A_{1}f_{12}-J_{2}A_{2}f_{21} \\
&=A_{1}f_{12}\Delta J_{1 / 2}
 \end{align}
$$
We can interpret this as describing a potential difference $\Delta J$ acting on a thermal “current” $\dot{Q}$ under a “space resistance” $\frac{1}{A_{1}f_{12}}$
$$
\dot{Q}_{12}=\frac{\Delta J_{1 / 2}}{R_{s}}
$$
Since EM-waves travel in straight lines, if radiation can travel from $i$ to $j$ along a path, it can reverse the path from $j$ to $i$. Therefore we have the reciprocity relationship
$$
A_{1}f_{12}=A_{2}f_{21}
$$

### Deviating from the lectures

We can similarly define an origin fraction $k_{ij}$ which is the fraction of energy arriving at $i$ that originates from $j.$ Then the radiative exchange is
$$
\begin{align}
\dot{Q}_{12}&=G_{1}A_{1}k_{12}-G_{2}A_{2}k_{21}\\
&=A_{1}k_{12}\Delta G_{1 / 2}
 \end{align}
$$
by applying reciprocity identically.

Recall that
$$
J=\varepsilon E^{\circ}_{b}+(1-\varepsilon)G
$$
Then the relationship between $k$ and $f$ is given by
$$
\begin{align}
\dot{Q}_{12}&=A_{1}k_{12}\Delta G_{1 / 2}=A_{1}f_{12}\Delta J_{1 / 2} \\
k_{21}&=f_{12}\left[ \frac{\Delta (\varepsilon E^{\circ}_{b})+\Delta((1-\varepsilon)G)}{\Delta G} \right] 
 \end{align}
$$
but this is overcomplicated for anything other than simple geometries.

### Shape factor algebra
The fractions of energy destinations $f_{i}$ add to unity.
$$
\sum_{j} f_{ij}=1
$$
Convex surfaces cannot see themselves so
$$
f_{i,i}=0\quad\forall i
$$
Reciprocity as previously,
$$
A_{1}f_{1,2}=A_{2}f_{2,1}
$$
These relationships apply to any diffuse radiation.
### Shape factor example
Consider the radiation exchange in the an L–section that extends infinitely into the page. Considering a virtual surface $4$ instead of the environment (considered surface $3$), we can find the $f_{1,2}$ by considering $f_{1,4}.$
![[radiative-shape-factor-example.png]]
### Concentric bodies
Consider convex body 1 contained within convex body 2. The overall space resistance is
$$
R_{s}= \frac{1-\varepsilon_{1}}{A_{1}\varepsilon_{1}}+ \frac{1}{A_{1}f_{1,2}}+\frac{1-\varepsilon_{2}}{A_{2}\varepsilon_{2}}
$$
where $f_{1,2}$ is $1$ due to the geometry.

Then the net power transfer is
$$
\begin{align}
\dot{Q}&=\frac{\Delta J}{R_{s}} \\
&= \frac{A_{1}\sigma\Delta(T^{4})_{1,2}}{\frac{1-\varepsilon_{1}}{\varepsilon_{1}}+1+\frac{A_{1}}{A_{2}} \frac{1-\varepsilon_{2}}{\varepsilon_{2}}}
 \end{align}
$$

Taking $A_{2}\to \infty$ we get an expression that looks like $A_{2}$ is a black body!

>When an object is in a large enclosure, the net radiation exchange is independent of the emissivity of the enclosure and is as if the enclosure was a black body.

### Radiation in the environment
The radiation re-emitted by the Earth is at a much lower frequency that the incident radiation. 

Incoming UV rays are absorbed by $\mathrm{O}_{3}$ and $\mathrm{O_{2}}.$

The re-emitted radiation is unfortunately at the right wavelength to be absorbed by greenhouse gases like $\ce{CO_{2}},$ $\ce{H_{2}O}$ and $\ce{CH_{4}}$.

![[env-rad.png]]
Let’s derive a simple model of this. Define the albedo $\alpha$ as the fraction of incident radiation that is reflected. 

Consider a planet of radius $R$ with incident solar flux $S.$ Consider its re-emission as a black body.

The incident absorbed energy is
$$
\dot{Q}_{s}=\pi R^{2}S(1-\alpha)
$$
If output long-wave flux is $H$ from the atmosphere, then the re-emitted energy is 
$$
\dot{Q}_{p}=4\pi R^{2}H
$$
At the steady state where $\dot{Q}_{s}=\dot{Q}_{p}$ in the atmospheric layer, then
$$
H= \frac{1-\alpha}{4}S
$$
Balancing energy at the planet ground level where $F$ is the atmospheric flux absorption gives
$$
\begin{align} \\
4\pi R^{2}F&=4\pi R^{2}H+(1-A)S\pi R^{2} \\
F&=H+ \frac{1-\alpha}{4}S \\
 \\
\Rightarrow\quad F&=\sigma T_{e}^{4}=\frac{1-\alpha}{2}S
 \end{align}
$$
Hence we can see the sensitivity to the atmospheric parameters!