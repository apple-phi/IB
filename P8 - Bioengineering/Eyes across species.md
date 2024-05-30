
## Evolution of the eye

The eye has evolved many times in many species!

Each evolutionary stage provides a selective advantage:
- Flat layer of light-sensitive receptors—sense light or dark
- Light-sensitive cup—sense light direction
- Pin-hole camera—sense the image more accurately (but at trade-off with illuminance)
- Lensed camera—focus the light without de-illuminating the image
- etc.

>c.f. the Richard Dawkins interview on this.

Given an aperture $a,$ and distances taken from the pin-hole, the point spread function is
$$
\Delta d=a\left( 1+ \frac{d_{\mathrm{retina}}}{d_{\mathrm{object}}} \right)
$$
![[eye-evolution.png]]
![[eye-pin-hole.png]]

## Lensing
Snell’s law
$$
n_{1}\sin\theta_{1}=n_{2}\sin\theta_{2}
$$

Focal length (take $r_{\mathrm{object}}\to \infty$ to see intuition)
$$
\frac{1}{f}= \frac{1}{r_{\mathrm{object}}}+\frac{1}{r_{\mathrm{retina}}}
$$

Lens-maker’s formula, given the curvatures $C=\frac{1}{R}$ of both sides of the lens
$$
\frac{1}{f}= \frac{r_{\mathrm{lens}}-r_{\mathrm{medium}}}{r_{\mathrm{medium}}}(C_{\mathrm{inner}}+C_{\mathrm{outer}})
$$

Matthiessen's ratio is the ratio $\frac{f}{R}$ between the distance from the centre of the lens to the retina, versus the lens radius.

## Spherical aberration

Spherical lenses don’t perfectly focus light—would need a parabola instead!

Solutions across species:
- An inhomogeneous lens—humans do this
- Multiple lenses (with the outer being parabolic)—*Pontella* does this
- Horizontal scanning of a telescopic eye—*Copilia* does this!


## Corneal refraction

Humans also have a cornea which provides most of the focussing power so the lens can just do fine-tuning!

>The human cornea doesn’t do a good job of correcting for spherical aberration.

Amphibians have a flat cornea and do all focussing dynamically using the lens.


## Negative lens

Birds see a very wide range of wavelengths so need robust way to correct for longitudinal chromatic aberration. 

![[avian-eye.png|400]]

## Mirrors

Cats’ eyes glow because they have a non-focussing reflective layer behind the retina to increase photon capture.

Scallops do their focussing almost entirely using a spherical mirror behind the retina. This places the focal point at about half the curvature radius, and that’s where the retina layer lies. Their lens is non-focussing but instead pre-corrects the spherical aberration due to the mirror.

![[scallop-eye.png|500]]
>The scallop lens is analogous to a Schmitt corrector plate.

## Compound eyes

Some species (insect, arachnids, etc.) have sub-eyes, each with their own optical apparatus, and are less able to do lens focussing dynamically.

The main limitation is diffraction! The point spread function is $\frac{2\lambda}{a}$ where $a$ is the aperture.

### Apposition eye
An image forms per ommatidium (sub-unit) and is apposed with the other images in the brain to form the visual image.

![[apposition.png]]
Low light sensitivity.
### Superposition
The photoreceptors are further away from the ommatidia and detect superposition of light rays entering through many different ommatidia.

Higher light sensitivity.

![[superposition-eye.png|600]]