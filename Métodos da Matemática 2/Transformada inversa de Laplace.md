


##### Exemplo
Use a fórmula complexa de inversão para calcular as seguintes transformada inversas

a) $$ \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{t^{-2/3}}{\Gamma{1/3}} $$
$\displaystyle \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{1}{2\pi i}\int_{\Gamma} \frac{e^{st}}{s^{1/3}}ds$ ;   $s^{1/3}=0$ => Multiplas raízes em $s=0$
$\displaystyle \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{1}{2\pi i}\int_{\infty}^0 r^{-1/3}e^{i\pi/3}e^{rt}dr +\frac{1}{2\pi i}\int_\infty^0  r^{-1/3}e^{-i\pi/3}e^{rt}dr$
$\displaystyle =\frac{1}{2\pi i}\left[ \int_0^\infty r^{-1/3}e^{i\pi/3}e^{rt}dr-\int_0^\infty r^{-1/3}e^{-i\pi/3}e^{rt}dr \right]=\frac{1}{2\pi i}\int_0^\infty e^{rt}r^{-1/3}\underbrace{e^{i\pi /3}-e^{-i\pi/3}}_{2isen(\pi/3)}$ 
$\displaystyle =\frac{1}{2\pi i}\int_0^\infty e^{rt}r^{-1/3}sen(\pi /3)dr=\frac{isen(\pi/3)}{\pi}\int_0^\infty  \underbrace{r^{2/3-1}e^{rt}dr}_{\begin{align} v=rt\\ dv=tdr \end{align}}=\frac{sen(\pi/3)}{\pi}\int_0^\infty \frac{v^{2/3-1}}{t^{2/3-1}}e^v \frac{dv}{t}$
$\displaystyle =\frac{sen(\pi/3)}{\pi t^{2/3}}\Gamma{(2/3)}=\frac{t^{-2/3}}{\Gamma{(1/3)}}$, usando  $\displaystyle \Gamma{(z)}\Gamma(1-z)=\frac{\pi}{sen(\pi z)}$
