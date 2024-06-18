
## 2D Optical imaging of the eye

### Introduction
- We’re doing ophthalmology (eye care) not optometry (eye correction)
- Focussing on *fundus* (the posterior segment of the eye) imaging
### Optics
![[fundus-imaging.png]]

Numerical aperture
$$
\mathrm{NA}=n\sin \theta
$$

where $n$ is the refractive index.

$f$-number
$$
N=\frac{f}{D}
$$
Their relationship is
$$
\begin{align}
\mathrm{NA}&=n\sin \arctan \frac{D}{2f} \\
&\approx \frac{1}{2}\frac{n}{N}
 \end{align}
$$

### Fundus imaging

With a relaxed (unaccommodated) eye, it is focussed at infinity so a matched focus at infinity on the ophthalmoscope will produce a sharp image of the fundus.

![[fundus-unaccomodated-imaging.png]]
In general the fundus camera must be adjusted by picking a lens to correct the patient’s focal imperfections.

The image is hindered by:
- The reflection of the flash
- Poor resolution

To avoid reflections off the cornea, the illumination is only through a circumferential annulus, with the reflection imaged through the centre.

Fundus cameras use green light since it produces a high contrast for blood vessels.

### Lens resolution

![[lens-calculations.png]]

Assume a light beam has a circular cross-section, and at the focus, the intensity varies normally with $x.$

$$
I(x)\propto \exp \left\{ -2\left( \frac{x}{r_{0}} \right)^{2} \right\} 
$$

The result is the the radius of this beam varies as the beam diverges as
$$
r(z)=\sqrt{ r_{0}^{2}+\left( \frac{\lambda z}{\pi} \right)^{2}  }
$$
where $\lambda$ is the wavelength and $r_{0}=r(0)$.

The radial resolution is the diameter of the focal spot.
$$
\Delta x=2r_{0}
$$

At the lens, $z=f$ and $r\approx \frac{D}{2}$ so
$$
\frac{D}{2}=\sqrt{ \left( \frac{\Delta x}{2} \right)^{2}+ \left( \frac{\lambda f}{\pi} \right)^{2} }
$$
Now $D\gg\Delta x$ so
$$
D= \frac{4\lambda f}{\pi\Delta x}
$$
so
$$
\Delta x= \frac{4\lambda f}{\pi D}
$$

Then in terms of numerical aperture of f-number is
$$
\Delta x= \frac{4\lambda N}{\pi}\approx \frac{0.64\lambda}{\mathrm{NA}}
$$

Tissue is translucent and scatters and attenuates the light. Hence the image is blurred axially (depth-wise) also. 

The axial resolution $\Delta z$ is the range in $z$ over which the beam area is at most twice the focal area, so
$$
r\left( z=\frac{\Delta z}{2} \right)=\sqrt{ 2 }r_{0}
$$
so using the previous equation for $r$ gives
$$
\Delta z= \frac{\pi\Delta x^{2}}{2\lambda}
$$
which again in terms of lens characteristic is
$$
\Delta z= \frac{8\lambda N^{2}}{\pi}\approx \frac{0.64\lambda}{(\mathrm{NA})^{2}}
$$

Hence alternative definition for $\mathrm{NA}$ is
$$
\mathrm{NA}\approx \frac{\Delta x}{\Delta z}
$$

Summary:
![[focussing-summary.png]]

### The Scanning Laser Ophthalmoscope (SLO)

The $\mathrm{SLO}$ cans over the retina to rasterize the image from many high res images, each at a specific 3D position,

![[SLO.png]]
The dichroic mirror only reflects the useful wavelengths of light.

>Note that the reflection and illumination is converse to the fundus camera. This gives a more accurate image, but laser safety places an upper bound on that the maximum laser power.

Scattered light will be filtered out with the confocal aperture to minimise noise. There is a trade off between filtering the noise and overly restricting the desired light rays—an upper bound on depth resolution.

Longer wavelengths near infrared are better for imaging deep structures since they have lower absorption coefficients.
## Optical Coherence Tomography (OCT)
We can take advantage of the spatial coherence of laser light to image the eye better! Normally this is an annoying phenomenon but it provides additional information we can extract.
![[light-coherence.png]]


### Michelson Interferometer
First used in 1887. Nowadays these are typically constructed using optical fibres instead of the light-splitter.
![[michelson.png]]

### OCT systems
![[Imaging the eye.png]]
Let the electric field from the laser be
$$
E_{l}(\omega)=E_{0}
(\omega)e^{ j\omega t }$$

with the reference signal (assuming an ideal mirror)
$$
E_{r}(\omega)=E_{0}(\omega)\exp \left\{ { j\omega\left( \frac{l_{r}}{c} -t\right) }  \right\}
$$

The signal $E_{s}$ from the object is
$$
E_{s}(\omega)=E_{0}(\omega)\int_{-\infty}^{\infty}\operatorname{r}_{s}(l_{s})\exp \left\{ { j\omega\left( \frac{l_{r}}{c} -t\right) }  \right\}  \, \mathrm{d}l_{s} 
$$

where $l_{s}$ is the round trip distance and $\operatorname{r}_{s}(l_{s})$ is the amplitude reflectivity density function with depth as a parameter.

The output of the interferometer is then the photo diode intensity due to superposition:
$$
\begin{align}
I(\omega)&=|E_{r}+E_{s}|^{2} \\
&=|E_{r}|^{2}+|E_{s}|^{2}+2\Re\left\{ E_{r}\overline{ E_{s}} \right\} 
 \end{align}
$$
### Time domain $\mathrm{OCT}$ systems
In time domain OCT, we’re only interested in the $2\Re\left\{ E_{r}\overline{ E_{s}} \right\}$ interference term. The photo diode measures the total intensity over al frequencies,
$$
I_{t}=\int_{-\infty}^{\infty} I(\omega) \, \mathrm{d}\omega
$$

Using Wiener-Khinchin theorem for autocorrelation, we can arrive at

tbc

- The $\cos$ term means that moving the mirrors modulates the intensity as an $\mathrm{AC}$ signal over depth.
- As we measure the amplitude envelope of the $\mathrm{AC}$ signal we recover the integral in the $\Re$ interference term
- The inner integral includes the desired distribution $\operatorname{r}_{s}(l_{s})$ over all depths, but the autocorrelation function $\operatorname{R}_{ee}$ is only non-zero close to zero, where $l_{r}\approx l_{s}$ so we end up recording $r_{s}$ close to the mirror position $l_{r}$
- The depth resolution is determined by the range of the autocorrelation function, which depends on the source power spectral density $S_{0}(\omega)$

![[time-oct-summary.png]]
![[time-oct-demo.png]]

The axial resolution matches the correlation length of the laser pulse. For a gaussian modulated pulse, this is
$$
\begin{align}
l_{c}&= \frac{2\ln_{2}}{\pi} \frac{\lambda_{0}^{2}}{\Delta\lambda} \\
&\propto \frac{\lambda_{0}^{2}}{\Delta\lambda}
 \end{align}
$$
where $\lambda_{0}$ is the centre wavelength and $\Delta\lambda$ is the [[bandwidth]].

Note the trade-off between getting results fast and varying the distance to the moving reference mirror slow enough to get a good precision.

But we’d like to not have any moving parts…
### Spectral OCT systems

tbc

## Ultrasonography of the eye

### Basic principles of ultrasonography
tbc
### System resolution and relationship to OCT
tbc

### Speed
Sound travels significantly slower in tissue, so the echo is important to consider. We can sample the echo *as it arrives!*

![[ultrasound-enveloped.png]]

Although the signal is a function of time, by assuming a constant speed we can convert it to a function of depth.

To focus the sound signal, the ultrasonic transducer is comprised of many piezoelectric components which each generate and receive the sound signal at slight delays so the sound wave interferes constructively at the desired focal point. 

![[sound-transducer.png]]

>This means we can set the focal point in 2D space dynamically.

To get a 3D image we can rotate the transducer using a stepper motor.

![[3D-ultrasound.png|250]]

### Resolution
Compared to OCT, ultrasound can see deeper into the retina with **less** resolution and **less** contrast. It is **more** complex but still has similar scanning times.

## Displaying 3D data

There are a few ways:

- **Reslicing**—show a 2D cross-section in a chosen location / orientation
	- easy but needs interpolation, and shadows can be confusing (since the pulse-echo direction isn’t shown)
- **Surface rendering**—show an iso-surface at a specific threshold
	- Marching cubes algorithm!
- **Volume rendering**—entire 3D dataset contributes to the 2D image
	- E.g. ray casting / ray marching 
	- Harder to $\mathrm{GPU}$ optimise
- Take characterising measurements directly from the data
	- Not intuitive, not powerful enough for complex measurements (cupping etc.)

Can combine techniques to show more data at once. E.g. texture map a reslice onto a 3D model.
