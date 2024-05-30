# 1.
$$
\begin{align}
Z_{i}&=R\parallel Z_{c}+Z_{l} \\
&=\left( \frac{1}{R_{1}}+j\omega C\right)^{-1}+R_{2+}j\omega L \\
&=12.734+8.838j \\
 \\
i&=\frac{|v|}{Z_{i}}=15.484\angle{-0.607} \\

\end{align}
$$
tbc

# 2.
$Q$ through capacitor is $v^{2}\omega C$ hence use
$$
C=\frac{Q_{1}}{v^{2}\omega}=\pu{ 117\mu F }
$$
All variables change except for any real power losses in the main circuit.

# 3.
For the $\Delta$ load, $V_{\Delta}=I_{\Delta}Z_{\Delta}$ hence
$$
\begin{align}
V_{l}&=\frac{I_{l}}{\sqrt{ 3 }}Z_{\Delta} \\
\Rightarrow\quad I_{l}&= \frac{\sqrt{ 3 }V_{l}}{Z_{\Delta}} \\
&=\pu{ 84.168A \angle-0.438}
 \end{align}
$$
The power transfer is then
$$
\begin{align}
P_{i}&=3I_{\Delta}^{2}R_{\Delta}\\
&= \frac{3V_{\Delta}^{2}R_{\Delta}}{|Z_{\Delta}|^{2}}  \\
&= \pu{ 1453kW } \\
 \\
Q_{i} &= \frac{3V_{\Delta}^{2}X_{\Delta}}{|Z_{\Delta}|^{2}}  \\ 
&=\pu{ 680kW } \\
 \\
\cos\phi&=\cos\left( \arctan\left( \frac{Q_{i}}{P_{i}} \right) \right) \\
&=0.906
 \end{align}
$$
# 4.
$$
\begin{align}
P_{i}&=\pu{ 14MW  } \\
Q_{i}&=\sum P\tan \phi \\
&= 6\tan (-\arccos 0.8) + 8\tan (\arccos 0.6) \\
&=\frac{37}{6} \\
 \\
\Rightarrow\quad \phi_{i}&=\cos\left( \arctan \frac{Q_{i}}{P_{i}} \right)=\pu{ 0.915lag } \\

\end{align}
$$
We know that
$$
3V_{p}I_{p}\cos \phi_{i}=P_{i}
$$
hence,
$$
I_{l}=\frac{P_{i}}{3V_{l}\cos \phi_{i}}=\pu{ 8031A }
$$
turbulence 
# 5.
$$
\begin{align}
P_{i}&=P_{t}+I_{l}^{2}R_{l} \\
Q_{i}&=Q_{t}+I_{l}^{2}X_{l}
 \end{align}
$$
Since $S_{i}^{2}=(3V_{l}I_{l})^{2}$ we then find that $V_{l}=\pu{ 153.7V }$
At unity power factor the line current is lower so there is less line heating loss.

# 6.


![[2P5 EP3 solutions.png]]