Como motivação, podemos considerar a [[função]] $\phi_N(x)$ definida como
$$\phi_N(x)=\begin{cases} \frac{N}{2},~~~~|x|<\frac{1}{N}\\0,~~~~|x|>\frac{1}{N} \end{cases}$$
Podemos calcular a [[Séries de Fourier]] da função $\phi_N(x)$ e obtemos
$$F[\phi_N(x)]=\frac{1}{2L}+\sum\limits_{n=1}^\infty \left( \frac{N}{n\pi} \sin\frac{n\pi}{NL}\right)\cos \frac{n\pi x}{L}$$
A função $\phi_N(x)$ tende a concentrar em apenas um ponto conforme N cresce, e quando analisamos a convergência da série de Fourier, obtemos que ela diverge para N -> $\infty$. Porém, se integrarmos teremos que a vale 
$$\lim_{n\to \infty}\int_{-L}^L \phi_N(x)dx=1$$

Assim, construímos a ''função'' delta de dirac palas suas propriedades de integração
$$\int_{-\infty}^\infty \delta(x)\phi(x)dx=\phi(0)$$

#### **[[Translação da função delta de dirac]]**
Seja uma operação de translação denotada por $\delta(x-a)$, obtemos que
$$\int_{-\infty}^\infty\delta(x-a)\phi(a)dx=\int_{-\infty}^\infty \delta(y)\phi(y+a)dy=\phi(a)$$  
### [[Mudança de escala da função delta de dirac]]
Uma operação de escala sendo definida como $\delta(ax)$
- Se $a>0$
$$\int_{-\infty}^\infty \delta(ax)\phi(x)dx=\frac{1}{a}\int_{-\infty}^\infty \delta(y)\phi(y/a)dy$$
- Se $a < 0$
$$\int_{-\infty}^\infty \delta(ax)\phi(x)dx=-\frac{1}{a}\int_{-\infty}^\infty \delta(y)\phi(y/a)dy$$
Então de modo geral
$$\int_{-\infty}^\infty \delta(ax)\phi(x)dx=\frac{1}{|a|}\int_{-\infty}^\infty \delta(y)\phi(y/a)dy$$
### [[Derivada da função delta de Dirac]]
Para definirmos a [[Derivada]], denotamos como $\delta'(x)$
$$\int_{-\infty}^\infty \delta'(x)\phi(x)dx=\underbrace{\delta(x)\phi(x)|_{-\infty}^\infty}_{\phi(x) \text{ é 0 nos extremos }} -\int_{-\infty}^\infty \delta(x)\phi'(x)dx=-\int_{-\infty}^\infty \delta(x)\phi'(x)=-\phi'(0)$$
### [[Primitiva da função delta de Dirac]]
Buscamos uma [[função]] $H(x)$, tal que $H'(x)=\delta(x)$
Essa função é conhecida como [[Função degrau]] ou qualquer função que converge para ela, como
- $H_n(x)=\frac{1}{2}+\frac{1}{\pi}arctan(nx)$
- $\displaystyle H_n(x)=\frac{1}{2}erfc(-nc)=\frac{1}{\sqrt{\pi}}\int_{-nx}^\infty e{-u^2}du$
- $H_n(x)=\displaystyle e^{-e^{-nx}}$
- $\displaystyle H_n(x)=\frac{1}{2}+\frac{1}{\pi}Si(nx)=\frac{1}{\pi}\int_{-\infty}{nx}\frac{\sin(u)}{u}du$



---
##### Exercício
Prove $\displaystyle \delta_n(x)=\frac{n}{\pi}\frac{1}{1+n^2x^2}$
Usando a definicao de delta para provar que o total é unitário $\displaystyle \lim_{n\to \infty}\int_{-\infty}^\infty \delta_n(x)dx=\lim_{n\to \infty}\int_{-\infty}^\infty \frac{n}{\pi}\frac{1}{1+n^2x^2}dx=\lim_{n\to\infty}\left[ \frac{n}{\pi}\int_{-\infty}^\infty \frac{1}{1+n^2x^2}dx \right]$
Tome $\begin{align} y=nx\\ dy=ndx \end{align}$ => $\displaystyle \lim_{n\to \infty}\left[ \frac{1}{\pi}\int_{-\infty}^\infty  \frac{1}{1+y^2}dy\right]=\lim_{n\to\infty} \left[ \frac{1}{\pi} Arctan(x)|_{-\infty}^\infty \right]=\lim_{n\to\infty} \left[ \frac{1}{\pi}(\frac{\pi}{2}-(\frac{\pi}{2}))\right]$ 
=$\lim_{n\to\infty} \left[\frac{\pi}{\pi}\right]=1$

$\displaystyle \lim_{n\to\infty} \int_{-\infty}^\infty \underbrace{\delta_n(x)}_{dv}\underbrace{\phi(x)dx}_{u} =\lim_{n\to\infty}\left[ \phi(x)Degrau(x)|_{-\infty}^\infty -\int_{-\infty}^\infty Degrau(x)\phi'(x)dx \right]$ 
$=\displaystyle \lim_{n\to\infty}\left[ 0-\left[ \underbrace{\int_{-\infty}^a Degrau(x)\phi'(x)dx}_{0}+\int_{a}^\infty Degrau(x)\phi'(x)dx\right] \right]$, se a funcão degrau muda de valor em a 
$\displaystyle =\lim_{n\to\infty}\left[ -\int_{b}^\infty \phi'(x)dx \right]=-\phi(x)|_a^\infty =-(-\phi(a))=\phi(0)$
##### Exercício
Prove $\delta_n(x)=\frac{n}{\sqrt{\pi}}e^{-n^2x^2}$
$\displaystyle \lim_{n\to\infty}\int_{-\infty}\infty \frac{n}{\sqrt{\pi}}e^{-n^2x^2} \underbrace{\rightarrow}_{\begin{align} y=nx \\ dy=ndx \end{align}}\lim_{n\to\infty} \int_{-\infty}^\infty f(y)dy=\int_{-\infty}^\infty f(y)dy=1$ 
##### Exercício
Prove $\delta(a-x^{-1})$, $f(x)=a-x^{-1}$
$f(x)=1-x^{-1}=0\Rightarrow a=\frac{1}{x}\Rightarrow \boxed{x=1/a}$
$f'(x)=-x^{-2}\Rightarrow f'(1/a)=-(1/a)^{-2}=-a^2$
$\delta[a-x^{-1}]=\frac{\delta(x-1/a)}{-a^2}$
##### Exercício
$\delta'(x^3+3x),~f(x)=x^3+3x$
$f(x)=x^3+3x=0\Rightarrow x(x^2+3)=0\Rightarrow x=0$
$f'(x)=3x^2+3,~f''(x)6x$

$\displaystyle \int_{-\infty}^\infty \delta'(g(x))\phi(x)dx\underbrace{\rightarrow}_{\begin{cases} y=y(x)\\ dy=y'(x)dx \end{cases}}\int_{-\infty}\infty \delta'(y)\phi(h(y))\frac{dy}{y'(h(y))}=(-1)\frac{d}{dx}\left[ \frac{\phi(h(y))}{y'(h(y))} \right]_{y=0}$
$\begin{cases} h(0)=r\Rightarrow g'(h(0))=g'(r)\\ h'(0)=1/g'(r) \end{cases}\Rightarrow \displaystyle \frac{d}{dy}\left[ \frac{1}{g'(h(y))}=\frac{-1}{[g'(h(y))]^2} \right]g''(h(y)).h'(y)$   
$=\displaystyle \frac{g''(h(y))}{[g'(h(y))]^2}\frac{1}{g'(h(y))}=\frac{g''(h(y))}{[g'(h(y))]^3}$
Então
$\displaystyle -1\left[ \frac{\phi'(h(y)).(\frac{1}{g'(h(y)}).g'(h(y))-g''(h(y)).\frac{1}{g'(h(y))}.\phi(h(y))}{[g'(h(y))]^2} \right]_{y=0}$ 
$-1\displaystyle\left[ \frac{\phi'(h(y))-g''(0)\left( \frac{1}{g'(0)} \right) \cdot h(0)}{[g'(0)]^2} \right] = -1\left[ \frac{\phi'(0)-6 \cdot 0 \cdot (1/3) \cdot 3}{3^2} \right] = \frac{\phi'(0)}{9}\Rightarrow \frac{\delta'}{9}$ 
##### Exercício
$\delta''(x^3+x),~~\begin{align}g(x)=x^3+x\\ g'(x)=3x^2+1\\ g''(x)6x\\ g'''(x)=6 \end{align}$
$\displaystyle\int_{-\infty}^\infty \delta''(y(x))\phi(x)dx=\int_{-\infty}^\infty \delta''(y)\phi(h(y))\frac{dy}{y'(x)}=(-1)^2\frac{d}{d^2x}\left[ \frac{\phi(h(y))}{y'(x)} \right]_{y=0}=\frac{d}{dx}\left[\frac{d}{dx} \frac{\phi(h(y))}{y'(x)}\right]_{y=0}$
$=\displaystyle \frac{d}{dx}\left[ \frac{\phi'(h(y)) . (1/g'(h))-\phi(h(y)) . g''(h). (1/g'(h))}{[g'(h)]^2} \right]=\frac{d}{dx}\left[ \frac{\phi'(h)}{[g'(h)]^3} \right]-\frac{d}{dx}\left[ \frac{\phi(h)g''(h)}{[g'(h)]^3} \right]$
$=\displaystyle \frac{\phi'(h(y)).[g'(h)]^2-\phi'(h).3[g'(h)].g''(h)}{[g'(h)]^6}=-\frac{[\phi(h)g''(h)+\phi(h)g'''(h)].[g'(h)]^2+\phi(h)g''(h).3g'(h)g''(h)}{[g'(h)]^6}$
$=\displaystyle \frac{\phi''(h)}{[g'(h)]^4}-\frac{\phi'(h)g''(h)}{[g'(h)]^5}-\frac{\phi(h)g''}{[g'(h)]^4}-\frac{\phi(h)g'''(h)}{[g'(h)]^4}+\frac{3\phi(h)g''(h).g''(h)}{[g'(h)]^5}$
Analisando as derivadas
$g(x)=x^3+x=0\Rightarrow x(x^2+1)=0\Rightarrow x=0$ é polo simples
$\begin{align} g(0)=0\\ h(0)=0\\ g'(0)=1\\ g''(0)=0\\ g'''(0)=6 \end{align}$
$\Rightarrow \delta''(x)-6\delta(x)$
