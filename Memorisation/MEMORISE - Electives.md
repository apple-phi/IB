## Bioengineering

### Imaging
Radial resolution $\Delta x$ is diameter of focal spot
$$
\Delta x=2r_{0}
$$
Axial resolution $\Delta z$ is range in $z$ where beam area less than twice focal area
$$
r\left( z=\frac{\Delta z}{2} \right)=\sqrt{ 2 }r_{0}
$$

$f$-number
$$
N=\frac{f}{D}
$$
Numerical aperture
$$
\begin{align}
\mathrm{NA}&=n\sin \theta =n\sin \arctan \frac{D}{2f}\approx \frac{1}{2}\frac{n}{N} \\
&= \frac{\Delta x}{\Delta z}
 \end{align}
$$
where $n$ is the refractive index.

$\mathrm{OCT}$ 
$$
\begin{align}
I(\omega)&=|E_{r}+E_{s}|^{2} \\
&=|E_{r}|^{2}+|E_{s}|^{2}+\underbrace{ 2\Re\left\{ E_{r}\overline{ E_{s}} \right\} }_{ \text{interested in for Time Domain OCT} }
 \end{align}
$$
Photodiode measures total intensity
$$
\int _{\mathbb{R}}I(\omega) \, \mathrm{d}\omega 
$$

![[oct-symbols.png]]
#### Time-domain $\mathrm{OCT}$ 

Depth resolution $\Delta z$ determined by extent of autocorrelation of the electric field $R_{ee}=R_{ee}\left( \frac{l_{r}-l_{s}}{c} \right)$ which is only nonzero close to $l_{r}\approx l_{s}.$ Entirely a function of source power spectral density $S(\omega)=|E_{0}(\omega)|^{2}$

Axial resolution $\Delta z$ = correlation length $l_{c}$ Gaussian-modulated envelope has
$$
\Delta z=l_{c}\propto 0.44\frac{\lambda_{0}^{2}}{\Delta\lambda}
$$
Process:
- Move reference mirror to scan over imaging depth while sending laser pulses
- $\mathrm{HPF}$ the interference signal intensity to just keep the $\mathrm{AC}$ depth-varying interference term 
- Do envelope detection over the $\mathrm{AC}$ signal to get the sample reflectivity (envelope amplitude)

#### Spectral $\mathrm{OCT}$ 
Split up interferometer light with diffraction grating to get all frequency components in parallel with a $\mathrm{CCD}$ array to quickly and directly measure $I(\omega).$

Spectral reflectivity
$$
r_{s}\left( \frac{l_{s}-l_{c}}{c} \right)=\mathscr{F}^{-1}\left\{ \frac{I_{\mathrm{interf.}}(\omega)}{S(\omega)} \right\} 
$$
Axial resolution similar to Time-domain $\mathrm{OCT}$ 
$$
\Delta z\approx \frac{\lambda_{0}^{2}}{\Delta\lambda}
$$
Total imaging depth
$$
d=S\Delta z
$$
Process:
- Fixed reference mirror
- Record calibration spectra
- Record interferometer spectrum
- Subtract calibration spectra to leave just interference spectrum

### Disease

Amplitude of accommodation (maximum variation in $P$),
$$
A=P_{\max}-P_{\min}
$$
![[Tissues in the eye#Cornea]]

![[Tissues in the eye#Tissue biomechanics]]
### Darcy’s Law for convection flow

The volumetric fluid flow rate $Q$ along a medium with length $L$ due to pressure difference $p$ through an area A with hydraulic permeability $\kappa$ is
$$
Q= \kappa\frac{ A}{L}p
$$

Fast transport requires $\kappa p\gg D$

> Analogy of permeability with conductivity!

The time constant of the fluid flow is given by
$$
\tau=\frac{L^{2}}{E\kappa}
$$
Intrinsic permeability

$$k=\eta \kappa$$


## Information

### Optimisation
#### Bellman-Ford algorithm

```python
def relax(u, v):
    if v.dist > u.dist + weight(u, v):
        v.dist = u.dist + weight(u, v)
        v.prev = u
        return True

for v in V:
    v.dist = inf
    v.prev = None
    
source.dist = 0
for _ in range(|V|):
    for (u, v) in E:
        relax(u, v)

for (u, v) in E:
    if relax(u, v):
	    print("A -ve weight cycle exists")
```
### Computer vision
#### Smoothing
- Removes high-frequency noise (which would be amplified by differentiation)
- Needed for *scale-selection*
- Gaussian is a $\mathrm{LPF}$ so satisfies this requirement with cut-off frequency $\omega_{c}=\frac{1}{\sigma}$
$$
\operatorname{g}_{\sigma}(t)\leftrightarrow \exp \left\{ -\frac{1}{2}\left( \omega\sigma \right)^{2} \right\} 
$$
- Consider an octave of smoothed images $S(\mathbf{x},\sigma)$ over scale-space $\sigma\in\Sigma$ of size $s$
$$
S(\mathbf{x}, \sigma)=I(\mathbf{x})*\operatorname{G}_{\sigma}(\mathbf{x})
$$
- Can do efficient smoothing because of Image Pyramid. Split up the 2D Gaussian into 1D Gaussians
$$
\operatorname{G}_{\sigma}(\mathbf{x})\mapsto \operatorname{g}_{\sigma}(x)*\operatorname{g}_{\sigma}(y)
$$
- Sample the scale-space $\Sigma$ *logarithmically*
$$
\sigma_{n}=2^{n/s}\sigma_{0}
$$
- Apply incremental blurs to increase $\sigma$
$$
\operatorname{g}_{(\sigma_{n+1})}=\operatorname{g}_{(\sigma_{n})}*\overbrace{ \operatorname{g}_{(\sigma_{k})}}^{ \text{small kernel} }
$$
- After $s$ convolutions,
$$
\sigma_{n+s}=2\sigma_{0}
$$
- Then do *Nyquist sub-sampling* to $\frac{1}{4}$ of original size 
- Repeat for the next octave with an appropriately scaled $\sigma_{k}.$

#### Difference of Gaussians (DoG)

The Laplacian of Gaussians is band-pass since derivatives are band-pass
$$
\frac{\mathrm{d}^{2} }{{\mathrm{d}x}^{2}} \{\operatorname{g}_{\sigma}\}\leftrightarrow -\omega^{2}\operatorname{G}_{\sigma}(\omega)
$$
Difference of Gaussians is a good approximation of applying this to an image
$$
S(\mathbf{x},\sigma+\eta)-S(\mathbf{x},\sigma)\approx\sigma^{2}\nabla^{2}S
$$
> Subtracting images in the same octave is efficient.
#### Key-points and Histogram of Gradients (HoG)

Localisation:
- Find $(x,y)$ extrema of $S(x,y,\sigma_{n})$
- Test the $(x,y)$ at neighbouring $\sigma_{n\pm 1}$ in the octave to find local max / min.

Sampling:
- Sample initial $16\times 16$ pixels around localised key-point
- Compute gradient of samples
- Form histogram of gradient magnitudes at each orientation in $10\degree$ increments
	- $|\nabla S|$ in each bin $\angle \nabla S$
- Smooth the HoG
- Resample $16\times16$ at orientation given by maximum of smoothed HoG
#### $\mathrm{SIFT}$ descriptor

- Sample $16\times 16$ patch at key-point size and orientation
- Calculate $\nabla S$ for each pixel
- Weight it by Gaussian about sample centre
- Compute $8$-bin HoG for each sub-block of $4\times 4$
- Vectorise the 16 HoGs into a vector of length $128$ 
- Normalise the descriptor and threshold to interval $[-0.2, +0.2]$
- Renormalise

#### $\mathrm{SIFT}$ invariance

$\mathrm{SIFT}$ has good invariance to different situations.

Use the $\mathrm{SLOPS}$ acronym:

- **S**cale—due to blob scaling which normalises size
- **L**ighting—due to gradients (illumination), normalisation (contrast), and thresholding (specularities)
- **O**rientation—due to HoG in key-point localisation
- **P**erspective—due to HoGs and 16 cells (but this is only weak invariance)
- **S**hielding (occlusion)—due to being a local descriptor avoiding boundaries

Limitations:
- perspective
- boundary occlusions
- cluttered backgrounds

#### Recovering the 3D positions
- camera geometry (projection matrix) / triangulation
- pose estimation—need at least 3 point correspondences

Compare descriptor in one image to two nearest neighbours (found by K-D tree) in second image using Euclidean distance. Accept match if ratio of distances $>0.7$


## Jail for awful content

![[this-fucking-slide.png]]