loquSeja $f(x)$ [[Função contínua por partes]] e com [[Derivada]]s laterais à esquerda e direita em todo intervalo real e tal que $\int_{-\infty}^\infty  |f(x)|dx<\infty$. Então vale a chamada Fórmula da integral de Fourier

$$\frac{1}{\pi}\int_{-\infty}^{\infty}\left\{\int_{-\infty}^\infty f(\xi)\cos(\alpha(\xi-x))d\xi\right\}d\alpha=\frac{1}{2}[f(x+0)+f(x-0)]$$
$$F(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty f(x)}e^{ikx}dx$$
$$F^{-1}(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty F(k)e^{-ikx}dk$$

#### Motivação
Lembrando que a fórmula da [[Séries de Fourier]] é $\displaystyle \large f(t) = \frac{a_0}{2}+ \sum_{n=1}^\infty a_n cos(nt) + \sum_{n=1}^\infty b_n sen(nt)$ com $\displaystyle \displaystyle a_n =  \frac{1}{L}\int_{-L}^L f(x)cos\left( \frac{n \pi x}{L} \right)$, $\displaystyle \displaystyle a_0 = \frac{1}{L}\int_{-L}^L f(x)dx$ e $\displaystyle \displaystyle b_n = \frac{1}{L} \int_{-L}^L f(x)sen \left( \frac{n \pi x}{L}\right)$
Aplicando que $\sin(x)=\cos(x-\frac{\pi}{2})$, simplificamos que
$$f(x)=\frac{1}{2L}\int_{-L}^L f(t)dt+\frac{1}{L}\sum\limits_{k=1}^\infty \int_{-L}^L f(t)\cos\left[\frac{k\pi}{L}(t-x)\right]dt$$
Analisando a convergência em absolutamente integrável $\displaystyle \int_{-\infty}^\infty |f(x)|dx<\infty$
$$\left| \frac{a_0}{2} \right|=\frac{1}{2L}\left| \int_{-L}^L f(t)dt \right|\leq \frac{1}{2L}\int_{-L}^L |f(t)|$$
Assim, $\displaystyle \lim_{L\to \infty}\frac{1}{2L}\int_{-L}^L |f(t)| =0$
Então
$$f(x) = \lim_{L\to\infty} \frac{1}{L}\sum\limits_{k=1}^\infty \int_{-L}^L f(t)\cos\left[\frac{k\pi}{L}(t-x)\right]dt$$
Tentaremos transformar em uma [[Integral de Riemann]]
Seja $\displaystyle F(\alpha_k)=\frac{1}{\pi}\int_{-L}^Lf(t)\cos[\alpha_k(t-x)]dt$ tal que $\alpha_k=\frac{k}{L}\pi$ => $\Delta \alpha_k=\frac{\pi}{L}$
$$f(x) = \lim_{L\to\infty} \frac{1}{L}\sum\limits_{k=1}^\infty \int_{-L}^L f(t)\cos\left[\frac{k\pi}{L}(t-x)\right]dt=\lim_{L\to \infty}  \sum\limits_{k=1}^\infty \frac{\pi}{L}F(\alpha_k)= \sum\limits_{k=1}^\infty F(\alpha_k)\Delta \alpha_k\to \int_{0}^\infty F(\alpha_k)d\alpha$$
Então começamos com uma [[função]] e a representamos para todo intervalo
$$f(x)=\int_0^\infty \frac{1}{\pi}\int_{-\infty}^\infty f(t)\cos[\alpha(t-x)]dtd\alpha$$
#### Exemplo
Sendo $f(x)=\frac{N}{a^2+x^2},a>0$, ache a transformada de Fourier
$$F(x)=\frac{N}{\sqrt{2\pi}}\int_{\infty}^{\infty} \frac{e^{ikx}}{a^2+x^2}dx=N\sqrt{\frac{\pi}{2}}\frac{e^{-ki}}{a}$$
Polos simples em $z=\pm ia$, pelo teorema dos resíduos

#### Propriedades

- Linearidade
$$F[af(x)+bg(x)]=aF[f(x)]+bF[g(x)]$$

- Deslocamento
$$\begin{align}F[f(x-a)]=e^{ika}F(k)\\ F[e^{-i\alpha x}f(x)]=F(k-a)\end{align}$$
- Escala
$$F[f(cx)]=\frac{1}{|c|}F(c/k)$$
- Derivada
$$\begin{align}F[f'(cx)]=-ikF(x)\\ F[xf(x)]=-iF'(x)\end{align}$$
- [[Identidade de Parseval]]
Conservacão do produto escalar
$$<f|g>=<F|G>$$
- [[Produto convolução]]
$$F[(f*g)(x)]=F(k)G(k)$$
