$$P_n(t)=\frac{(2n)!}{2^n(n!)^2}p_n(t)=\frac{1}{2^nn!}\frac{d^2}{dt^n}(t^2-1)^n$$
$$\|P_n\|=\sqrt{\frac{2}{2n+1}}$$
- é solução da [[Equação de Legendre]] de forma $(1-x^2)y''-2xy'+v(v+1)y=0$
os primérios 6 termos são

| n   | $P_n(x)$                                             |
| --- | ---------------------------------------------------- |
| 0   | $1$                                                  |
| 1   | $x$                                                  |
| 2   | $\frac{1}{2}(3x^2-1)$                                |
| 3   | $\frac{1}{2}(5x^3-3x)$                               |
| 4   | $\frac{1}{8}(35x^4-30x^2+3)$                         |
| 5   | $\frac{1}{8}(63x^5-70x^3+15x)$                       |
| 6   | $\frac{1}{16}(231x^6-315x^4+105x^2-5)$               |
| 7   | $\frac{1}{16}(429x^7-693x^5+315x^3-35x)$             |
| 8   | $\frac{1}{128}(6435x^8-12012x^6+6930x^4-1240x^2+35)$ |


#### Expandindo uma função qualquer
Objetivo é representar uma [[função]] qualquer em torno de [-1, 1]
$$f(x)=\sum\limits_{n=0}^\infty a_nP_n(x)$$
onde $P_n$ são polinômios de legendre de grau n e $a_n$ são os coeficientes
cada coeficiente pode ser encontrada como
$$a_n=\frac{2n+1}{2}\int_{-1}^1 f(x)P_n(x)dx$$
#### Expandindo $x^2$
- Usamos a parte par $\displaystyle \int_{-1}^1x^2P_n(x)dx=0$
para n=0
$\displaystyle a_0=\frac{1}{2}\int_{-1}^1 x^2.1dx=\frac{1}{2}\int_{-1}^1x^2dx=\frac{1}{3}$, visto que $P_0(x)=1$
 $a_2=\frac{5}{2}\int_{-1}^1 x^2\frac{1}{2}(3x-1)dx=\frac{5}{4}\int_{-1}^1(3x^4-x^4)dx=\frac{2}{3}$

#### Expandindo $\begin{cases}-1,~~x<0\\ 1,~x>=0\end{cases}$
Também calcule $f(x)=\sum\limits_{n=0}^\infty C_nP_n(x)$ e $\sum\limits_{k=0}^\infty (4k+3)\left[\frac{(2k-1)!!}{(2k+2)!!}\right]^2$
 