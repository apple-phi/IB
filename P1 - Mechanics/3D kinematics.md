Recall the property of rotating vectors that
$$
\dot{\mathbf{r}}=\frac{\mathrm{d} \mathbf{r}}{\mathrm{d}t} +\boldsymbol{\omega} \times \mathbf{r}
$$
Then the acceleration is
$$
\begin{align}
\ddot{\mathbf{r}} & =\overbrace{ \frac{ \mathrm{d}^{2}\mathbf{r} }{ \mathrm{d}t^{2} } +\boldsymbol{\omega}\times \frac{\mathrm{d} \mathbf{r}}{\mathrm{d}t}}^{ \frac{\mathrm{d} }{\mathrm{d}t}\left( \frac{\mathrm{d} \mathbf{r}}{\mathrm{d}t}  \right)   } +\overbrace{ \frac{\mathrm{d} \boldsymbol{\omega}}{\mathrm{d}t} \times \mathbf{r}+\boldsymbol{\omega}\times\frac{\mathrm{d} \mathbf{r}}{\mathrm{d}t} +\boldsymbol{\omega} \times(\boldsymbol{\omega} \times \mathbf{r})}^{ \frac{\mathrm{d} }{\mathrm{d}t} \left( \boldsymbol{\omega} \times \mathbf{r} \right)  } \\
 \\
&= \underbrace{ \frac{ \mathrm{d}^{2}\mathbf{r} }{ \mathrm{d}t^{2} }}_{ \text{radial} } +\underbrace{ \frac{\mathrm{d} \boldsymbol{\omega}}{\mathrm{d}t} \times \mathbf{r}}_{ \text{tangential} }+\underbrace{ 2\boldsymbol{\omega}\times \frac{\mathrm{d} \mathbf{r}}{\mathrm{d}t}}_{ \text{Coriolis} } +\underbrace{ \boldsymbol{\omega}\times(\boldsymbol{\omega}\times \mathbf{r})}_{ \text{centripetal} }
 \end{align}
$$

## Gyroscopic mechanics
Consider a rotor with angular momentum $\mathbf{h}=J\boldsymbol{\omega}$ where $J$ is the polar moment of inertia. Then the corresponding torque $\mathbf{Q}=\dot{\mathbf{h}}$ required to turn the axis $\hat{\boldsymbol{\omega}}$ of the rotor by angular velocity $\boldsymbol{\Omega}$ is
$$
\begin{align}
\mathbf{Q}=\dot{\mathbf{h}}&= \frac{\mathrm{d} \mathbf{h}}{\mathrm{d}t} +\boldsymbol{\Omega}\times \mathbf{h} \\
&=J \dot{\boldsymbol{\omega}}+\boldsymbol{\Omega}\times J\boldsymbol{\omega}
 \end{align}
$$
If $\dot{\boldsymbol{\omega}}=0$ then
$$
\mathbf{Q}=\boldsymbol{\Omega}\times J\boldsymbol{\omega}
$$
> TODO—check if it is actually *polar* moment of inertia here???