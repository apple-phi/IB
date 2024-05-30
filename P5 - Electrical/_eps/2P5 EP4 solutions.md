## 1.
Since $S=3VI_{\mathrm{rated}},$ we have
$$
I_{\mathrm{rated}}=\frac{S}{3V}=\frac{\pu{500M}}{3\cdot \pu{ 60k } / \sqrt{ 3 }}=\pu{ 4811A }
$$
Under generator convention,
$$
\tilde{E}=\tilde{V}+j\tilde{I}X_{s}
$$
Hence the magnitude of phase $\tilde{E}$ is
$$
\begin{align}
|\tilde{E}|_{\mathrm{phase}}&=\left| |\tilde{V}|+X_{s}I_{\mathrm{rated}}\angle\left( \frac{\pi}{2}+\phi \right) \right| \\
&=\pu{21292V}
 \end{align}
$$
which as line $\mathrm{EMF}$ is
$$
|\tilde{E}|_{\mathrm{line}}=\pu{ 36879V }
$$
Conserving reactive power,
$$
\begin{align}
E\sin\delta&=IX_{s}\cos \phi \\
\Rightarrow\quad \delta&=\pu{40.6\!\degree}
 \end{align}
$$
## 2.
Begin with the phase current,
$$
\begin{align}
I_{\mathrm{rated}}&=\frac{S}{3V_{\mathrm{ph}}} \\
&=\frac{\pu{ 250M }}{3\cdot \pu{ 22k }/\sqrt{ 3 }} \\
&=\pu{ 6561A }
 \end{align}
$$
Then the excitation at unity power factor is
$$
\begin{align}
|E|_{\mathrm{ph}}&=\sqrt{ V^{2}+(IX_{s})^{2} } \\
&=\sqrt{ \frac{22000^{2}}{3}+(6561\cdot 1.2)^{2} } \\
&=\pu{ 14944V }
 \end{align}
$$
Hence the 15% increased excitation is $|E|_{\mathrm{ph}}'=\pu{ 17186V }.$ This corresponds to an increase in $E$ parallel to $\tilde{V}.$ From the voltage triangle we have
$$
\begin{align}
|E|'\sin\delta'&=IX_{s} \\
\Rightarrow\quad \delta'&=\pu{27.3\!\degree}
 \end{align}
$$
The amount that $E'$ is greater than $E$ is the new real part of the $j\tilde{I}'X_{s}$ term. Therefore
$$
\begin{align}
I'&=\frac{1}{X_{s}}\left| |E|'\cos\delta'-|\tilde{V}|+ jIX_{s} \right|  \\
&=\pu{ 6902A }
 \end{align}
$$
The power factor is now
$$
\begin{align}
\cos \phi'&= \frac{I}{I'} \\
&=\pu{0.951lag}
 \end{align}
$$
## 3.
$V, X_{s}$ kept constant and $I, \delta, \phi$ varied (but co-dependent). Since the excitation is constant,
$$
\begin{align}
P''&=\frac{3V''E'}{X_{s}}\sin\delta'' \\
\Rightarrow\quad \delta''&=\pu{33.3\!\degree } \\
\end{align}
$$
Applying the cosine rule,
$$
\begin{align}
|\tilde{I}|&=\frac{1}{X_{s}}\sqrt{ E^{2}+V^{2}-2EV\cos\delta } \\
&=\pu{7984A}
 \end{align}
$$
Conserving reactive power,
$$
\begin{align}
|E|\sin\delta&=|\tilde{I}|X_{s}\cos \phi \\
\Rightarrow\quad \cos \phi&=\pu{0.985lag}
 \end{align}
$$
## 4.
Scale the phasor diagram by $\frac{3V}{X_{s}}.$ The prime-mover limit is $\frac{3V^{2}}{X_{s}}=\pu{ 435.6MVAR }.$ The rotor heating limit is $\frac{3VE_{\max}}{X_{s}}=\pu{ 891MVA }.$ The stator heating limit (the rated $\mathrm{VA}$ is $\pu{ 500MVA }$).

tbc

## 5.
$$
\begin{align}
\mathrm{VA}_{b}&=3 \frac{V_{b}}{\sqrt{ 3 }}I_{b} \Rightarrow\quad  I_{b}=\pu{437.4A} \\
\mathrm{VA}_{b}&= \frac{V^{2}_{b}}{Z_{b}}\Rightarrow\quad Z_{b}=\pu{171.2\Omega}
 \end{align}
$$
Then the questioned values can be expressed as
$$
\begin{align}
\pu{125MVA}&=\pu{1.25pu} \\
\pu{107kV}&=\pu{0.81pu} \\
\pu{35\Omega}&=\pu{0.2pu} \\
\pu{950A}&=\pu{2.17pu}
\end{align}
$$
Converting the second set of questioned values into being relative to the second set of bases,
$$
\begin{align}
V&=\pu{1.58pu} \\
Z&=0.35\cdot \frac{75}{100}\cdot\left(  \frac{132}{100} \right)^{2}=\pu{0.457pu} \\
I&=\pu{0.91pu} \\
MVA&=\pu{2.13pu}
\end{align}
$$
## 6.
Choose $\mathrm{MVA}_b=\pu{100MVA}$ and $\mathrm{VA}_b$ is as transformer rated.

Convert transformer reactance:
$$
X=0.18\cdot \frac{100}{125}=0.144
$$
For line, 
$$
Z_{b}= \frac{V_{b}^{2}}{\mathrm{VA}_{b}}=174.2
$$
Thus
$$
X_{\mathrm{line}}=\frac{20}{174.2}=0.115pu
$$
Then
$$
\begin{align}
I_{\mathrm{load}}=\frac{P}{\sqrt{ 3 }V_{l}\cos \phi}=4887.6 \\
I_\text{base(load)} =\frac{100M}{\sqrt{ 3 }11k}=5248
 \end{align}
$$
Hence
$$
\begin{align}
I_\text{load }&=0.931pu \\
V_{\mathrm{load}}&=0.9545pu \\
Z\mathrm{_{load}}&=1.0251pu \\
\tilde{Z}\mathrm{_{load}}&=Z_{load}\operatorname{cis}\phi =0.9225+j 0.447
\end{align}
$$
Then
$$
E=I_{load}Z_{in(pu)}=1.605pu
$$

tbc recap
## 7.
Choose 1000MVA base.
MVA_sc= 1/(0.7+0.2)pu=1.111pu=1111MVA

So
$$
I_{sc}=\frac{MVA_{sc}}{\sqrt{ 3 }V_{b}}=4860A
$$
tbc
## 8.

tbc