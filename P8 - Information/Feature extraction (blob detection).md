## Keypoint detection (SIFT)
A different sample frequency is applied to each image within an octave, and different amounts of smoothing are applied to each octave.

![[keypoint-detection.png]]
![[scale-space.png]]
![[matching-keypoints.png]]
## Zero Normalized Patches

## Orientation histograms

## Why the DoG?

3 common related techniques:
- Laplacian of Gaussian
- Difference of Gaussians
- Convolution with Mexican Hat / Ricker wavelet

The DoG is an approximation to the LoG. It’s effectively single, non-separate convolution, but is commonly used instead of LoG because it naturally appears in a scale space setting where the image is filtered at many scales (Gaussians with different sigmas)—the difference between subsequent scales is a DoG. For image $f$ and Gaussians $\operatorname{g},$
$$
\nabla^{2}f\approx f*(g_{1}-g_{2})
$$

The DoG is a tuneable band-pass filter, while the LoG is not tuneable (being a purely differentiation operator). When the difference between $\sigma$’s tends to zero, the DoG tends to the LoG.

[image processing - What Is the Difference between Difference of Gaussian, Laplace of Gaussian, and Mexican Hat Wavelet? - Signal Processing Stack Exchange](https://dsp.stackexchange.com/a/47909)

