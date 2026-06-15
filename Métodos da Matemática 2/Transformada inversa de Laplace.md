A transformada inversa é definida por
$$f(t)H(t)=\mathcal{L}^{-1}[F(t)]=\frac{1}{2\pi i}\int_{\gamma -i\infty}^{\gamma+i\infty} e^st F(s)ds$$
onde $\gamma\in\mathbb{R}$   deve ser escolhido de modo que todas as possíveis singularidades de $e^{st}F(s)$ fiquem à esquerda de $\gamma$ no plano complexo e $H(t)$ ]é a funcao de Heaviside

Um caso ilustrador
Usar a fórmula de inversão para calcular o valor abaixo$$f(t)=\mathcal{L}^{-1}\left[ \frac{1}{s(s^2+\omega^2)} \right]$$
obtemos $\displaystyle f(t)=\frac{1}{2i\pi}\lim_{R\to\infty}\int_{\gamma-iR}^{\gamma+iR}\frac{1}{s(s^2+\gamma^2)}e^{st}ds$, para este caso consideramos o contorno de Bromwich, como a figura abaixo

![[contorno.png|365]]
Essa funcao apresenta polo simples sobre o eixo imaginário, então com $R>0$, está aceitável. Usamos resíduos para calcular sobre cada uma
$\displaystyle f(t)=Res_{s=0}f(s)+Res_{s=i\omega}f(s)+Res_{s=-i\omega}f(s) =\frac{2}{\omega^2}\sin^2\left(\frac{\omega t}{2}\right)$

##### Exemplo
Use a fórmula complexa de inversão para calcular as seguintes transformada inversas

a) $$ \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{t^{-2/3}}{\Gamma{1/3}} $$
$\displaystyle \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{1}{2\pi i}\int_{\Gamma} \frac{e^{st}}{s^{1/3}}ds$ ;   $s^{1/3}=0$ => Multiplas raízes em $s=0$
$\displaystyle \mathcal{L}^{-1}\left[ \frac{1}{s^{1/3}} \right]=\frac{1}{2\pi i}\int_{\infty}^0 r^{-1/3}e^{i\pi/3}e^{rt}dr +\frac{1}{2\pi i}\int_\infty^0  r^{-1/3}e^{-i\pi/3}e^{rt}dr$
$\displaystyle =\frac{1}{2\pi i}\left[ \int_0^\infty r^{-1/3}e^{i\pi/3}e^{rt}dr-\int_0^\infty r^{-1/3}e^{-i\pi/3}e^{rt}dr \right]=\frac{1}{2\pi i}\int_0^\infty e^{rt}r^{-1/3}\underbrace{e^{i\pi /3}-e^{-i\pi/3}}_{2isen(\pi/3)}$ 
$\displaystyle =\frac{1}{2\pi i}\int_0^\infty e^{rt}r^{-1/3}sen(\pi /3)dr=\frac{isen(\pi/3)}{\pi}\int_0^\infty  \underbrace{r^{2/3-1}e^{rt}dr}_{\begin{align} v=rt\\ dv=tdr \end{align}}=\frac{sen(\pi/3)}{\pi}\int_0^\infty \frac{v^{2/3-1}}{t^{2/3-1}}e^v \frac{dv}{t}$
$\displaystyle =\frac{sen(\pi/3)}{\pi t^{2/3}}\Gamma{(2/3)}=\frac{t^{-2/3}}{\Gamma{(1/3)}}$, usando  $\displaystyle \Gamma{(z)}\Gamma(1-z)=\frac{\pi}{sen(\pi z)}$
