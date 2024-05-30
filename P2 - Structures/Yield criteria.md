In both of the basic models, shear governs yielding:
- a *hydrostatic* stress state has $\sigma_{1}=\sigma_{2}=\sigma_{3}$ so induces no shear on any plane (the Mohr’s circle is just a point on the $\sigma$-axis) so does not yield
- this is the microstructural basis of [[plasticity]]—metal [[plasticity]] originates from dislocation movement driven by shear stresses
- this mechanism of plastic deformation does not require a volume change

These observations are confirmed experimentally for metals but may not universally apply to, e.g., foams.
## Tresca
This is physically based on the critical *maximum shear stress*.
$$
\max(|\sigma_{1}-\sigma_{2}|,|\sigma_{2}-\sigma_{3}|,|\sigma_{3}-\sigma_{1}|) \leq \sigma_{y}
$$
Under pure shear, i.e., $\sigma=\{ \pm k, 0 \}$ this leads to the following yield identity:
$$
k= \frac{\sigma_{y}}{2}
$$
## von Mises
This is physically based on the critical *elastic shear strain energy*.$$
(\sigma_{1}-\sigma_{2})^{2}+(\sigma_{2}-\sigma_{3})^{2}+(\sigma_{3}-\sigma_{1})^{2}\leq 2{\sigma_{y}}^{2}
$$Under pure shear, i.e., $\sigma=\{ \pm k, 0 \}$ this leads to the following yield identity:$$
\begin{align}
(2k)^{2}+(-k)^{2}+k^{2} & =2{\sigma_{y}}^{2} \\
 \\
\Rightarrow\quad k & = {\frac{\sigma_y}{\sqrt{ 3 }}} \\
 & \approx 0.5773\ \sigma_{y}
\end{align}
$$