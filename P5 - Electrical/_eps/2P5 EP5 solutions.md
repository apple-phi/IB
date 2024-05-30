## 1.
Test (b) is the locked rotor test. This implies slip $s=1$ so the magnetising terms $R_{0}$ and $X_{m}$ can be considered negligible. 
  
![locked-rotor-test.png|600](app://11a1915ef5ae6a1aafbc6df5e2e6e50f57fa/C:/Users/lucas/OneDrive/Documents/IB/P5%20-%20Electrical/_assets/locked-rotor-test.png?1708335575896)

Assuming $X_{1}=X_{2}'$ as given, conserve power.
$$
\begin{align}
P&=I^{2}(R_{1}+R_{2}') \\
R_{2}'&= \frac{4860}{(60\sqrt{ 3 })^{2}} \\
&=\pu{0.15\Omega}
 \end{align}
$$
Similarly conserving reactive power,
$$
\begin{align}
\sqrt{ (VI)^{2}-P^{2} }&= I^{2}(X_{1}+X_{2}') \\
X_{1}=X'2&=\frac{\sqrt{ (65\cdot60\cdot \sqrt{ 3 })^{2}-4860^{2} }}{2(60\sqrt{ 3 })^{2}} \\
&=\pu{0.217\Omega}
 \end{align}
$$
For test (a) we can assume that $s\approx0$ so the equivalent resistance $\frac{R_{2}'}{s}\approx0.$ We can also assume that $Z_{1}\ll R_{0}\parallel X_{m}$ hence the only impedance for the current is $R_{0}\parallel X_{m}.$ Conserving power,
$$
\begin{align}
P&=\frac{V^{2}}{R_{0}} \\
R_{0}&= \frac{415^{2}}{1720}=\pu{100.1\Omega}
 \end{align}
$$
Similarly, conserving reactive power,
$$
\begin{align}
\sqrt{ (VI)^{2}-P^{2} }&=\frac{V^{2}}{X_{0}} \\
X_{0}&= \frac{415^{2}}{\sqrt{ 3(415\cdot 6.5)^{2}-1720^{2} }} \\
&=\pu{39.65\Omega}
 \end{align}
$$

## 2.
For peak torque, by maximum power transfer theorem we have
$$
\frac{R_{2}'}{s}=\sqrt{ R_{1}^{2}+(X_{1}+X_{2}')^{2} }
$$
where $s=\frac{\omega_{s}-\omega_{r}}{\omega_{s}}$ and $\omega_{s}=\frac{\omega}{p}=25\pi\ \pu{rad s-1}=\frac{360}{2\pi \cdot 3}\cdot25\pi\ \pu{rpm}=\pu{1500rpm}.$ So the speed the torque is delivered at is
$$
\begin{align}
\omega_{r}&=\omega_{s}\left( 1- \frac{R_{2}'}{\sqrt{ R_{1}^{2}+(X_{1}+X_{2}')^{2} }} \right) \\
&=1500\left( 1- \frac{0.6}{\sqrt{ 0.5^{2}+2.8^{2} }} \right) \\
&=\pu{1184rpm}
 \end{align}
$$
Hence the peak torque is
$$
\begin{align}
T_{\max}&= \frac{3\tilde{I}^{2}_{2}}{\omega_{s}}\frac{R_{2}'}{s}  \\
&=\frac{3}{\omega_{s}} \left( \frac{\tilde{V}_{2}}{\sqrt{ \left( R_{1}+\frac{R_{2}'}{s} \right)^{2}+(X_{1}+X_{2}')^{2} }} \right)^{2}\frac{R_{2}'}{s}\\
&=\frac{3}{\omega_{s}} \left( \frac{\tilde{V}_{2}}{\sqrt{ \left( R_{1}+\sqrt{ R_{1}^{2}+(X_{1}+X_{2}')^{2} } \right)^{2}+(X_{1}+X_{2}')^{2} }} \right)^{2}\sqrt{ R_{1}^{2}+(X_{1}+X_{2}')^{2} } \\
&=\frac{3}{\frac{100\pi}{2}}\left( \frac{\frac{415}{\sqrt{ 3 }}}{\sqrt{ \left(0.5+\sqrt{ 0.5^{2}+2.8^{2} }\right)^{2} }+2.8^{2}} \right) \sqrt{ 0.5^{2}+2.8^{2} } \\
&=\pu{163.9Nm}
 \end{align}
$$

>Supo question: why is $\omega_{s}$ divided by two here in the cribs? 

## 3.
$$
\begin{align} 
\frac{R_{2}'}{s}&=\frac{0.74}{0.03}=\pu{24.67\Omega} \\
\omega_{s}&=\frac{\omega}{p}=\frac{2\pi \times50}{3}=\pu{104.7rad/s }\\
N_{r}&=\frac{\omega_{r}}{\omega_{s}}N_{s} \\
&=(1-s)N_{s} =(1-0.03)\cdot 1500=\pu{970rpm} \\
Z_{i}&=Z_{1}+(Z_{2}\parallel jX_{m})=21.7+j\pu{11.7\Omega} \\
I_{s}&=\frac{V}{Z_{i}}=8.55j\pu{4.612\Omega} \\
I_{2}'&=\frac{\frac{Z_{i}-Z_{1}}{Z_{i}}V}{Z_{2}}=8.756-j \pu{0.777A} \\
I_{2}&=1.5I_{2}'=\pu{8.97A} \\
T&=\frac{3}{\omega_{s}}I_{2}' \frac{R_{2}'}{s}=\pu{54.6Nm} \\
T_{\ell}&= \frac{P_{\ell}}{\omega_{r}}= \frac{P_{\ell}}{(1-s)\omega_{s}}=\pu{3.35Nm} \\
P_{o}&=(T-T_{\ell})\omega_{r}=\pu{5206W} \\
\cos \phi&=\cos (\arctan\angle I_{1})=\pu{0.8802lag} \\
P_{i}&=3VI_{1}\cos \phi=\pu{6150W }\\
\eta&=\frac{P_{o}}{P_{i}}=84.65\%
 \end{align}
$$
## 4.
The maximum output torque occurs when $\frac{R_{2}'}{s}$ matches the equivalent impedance of the rest of the circuit,
$$
\begin{align}
\frac{R_{2}'}{s}&= |\overbrace{ jX_{2}'+(Z_{1}\parallel jX_{m})}^{ Z_{\mathrm{Th}} }|=\pu{3.3124\Omega} \\
s&=\frac{R_{2}'}{|jX_{2}'+(Z_{1}\parallel jX_{m})|}=0.2234 \\
N_{r}&=(1-s)N_{s}=(1-0.2234)\cdot 1000=\pu{776.6rpm} \\
T_{\max}&=\frac{3}{\omega_{s}}I_{2}' \frac{R_{2}'}{s} \\
&= \frac{3}{2\omega_{s}} \frac{V_{\mathrm{Th}}^{2}}{R_{\mathrm{Th}}+Z_{\mathrm{Th}}}=\pu{161.5Nm}
 \end{align}
$$
where $V_{\mathrm{Th}}$ is given by
$$
V_{\mathrm{Th}}=\frac{VX_{m}}{|Z_{1}+jX_{m}|}=\pu{230.74V}
$$

For maximum output power, make the component subdivision $\frac{R_{2}'}{s}=R_{2}'+ \frac{1-s}{s}R_{2}'$ and apply maximum power transfer theorem as before, imposing
$$
\begin{align}
\frac{1-s}{s}R_{2}'&=|Z_{\mathrm{Th}}+R_{2}'| \\
s&=0.1671
 \end{align}
$$
For maximum starting torque at $s=1,$ require that
$$
\begin{align}
s_{m}&= \frac{R_{2}'}{Z_{\mathrm{Th}}}=1 \\
R_{2}'&=3.3124
 \end{align}
$$
which needs an extra referred rotor impedance of $\pu{2.5724\Omega}.$ This is an actual extra rotor resistance of
$$
\frac{2.5724}{1.5^{2}}=\pu{1.14\Omega}
$$
