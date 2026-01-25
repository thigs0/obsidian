Como motivação, podemos considerar a [[função]] $\phi_N(x)$ definida como
$$\phi_N(x)=\begin{cases} \frac{N}{2},~~~~|x|<\frac{1}{N}\\0,~~~~|x|>\frac{1}{N} \end{cases}$$
Podemos calcular a [[Séries de Fourier]] da função $\phi_N(x)$ e obtemos
$$F[\phi_N(x)]=\frac{1}{2L}+\sum\limits_{n=1}^\infty \left( \frac{N}{n\pi} \sin\frac{n\pi}{NL}\right)\cos \frac{n\pi x}{L}$$
A função $\phi_N(x)$ tende a concentrar em apenas um ponto conforme N cresce, e quando analisamos a convergência da série de Fourier, obtemos que ela diverge para N -> $\infty$. Porém, se integrarmos teremos que a vale 
$$\lim_{n\to \infty}\int_{-L}^L \phi_N(x)dx=1$$

Assim, construímos a ''função'' delta de dirac palas suas propriedades de integração
$$\int_{-\infty}^\infty \delta(x)phi(x)dx=\phi(0)$$

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

