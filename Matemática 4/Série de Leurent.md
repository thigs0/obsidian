Suponha que a função f é [[Holomorfa]] em um domínio $R_1 < |z-z_0|<R_2$, centrada no $z_0$ e uma [[Séries de Potências]] envolvendo as potências positivas e negativas de $z-z_0$, quando a função falha em ser Holomorfa em $z_0$
$$f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n+\sum_{n=1}^{\infty}\frac{b_n}{(z-z_0)^{n}} \hspace{2cm}(R_1 <|z-z_0|<R_2)$$
Onde:
$\displaystyle a_n = \frac{1}{2\pi i}\int_c \frac{f(z)dz}{(z-z_0)^{n+1}}$ 
$\displaystyle b_n = \frac{1}{2 \pi i}\int_c \frac{f(z)dz}{(z-z_0)^{-n+1}}$
Em outras palavras, se um domínio interno pode ser expresso em série de potência, existe uma curva tal que o complementar dela pode ser expresso por séries negativas de potência

---
- Se $z_0$ é singularidade isolada, se $0 \leq |z-z_0|<R$ 
- A singularidade isolada pode ser em uma quantidade finita
Então $\displaystyle \sum_{n=0}^\infty C_n(z-b)^n = f(z)$
resíduo


---
**Exemplo**
$\displaystyle f(z) = \frac{1}{z^5(z^{2}+9)}= \frac{1}{z^5}\frac{1}{z^2+9}$ $\displaystyle \frac{1}{2}\frac{1}{z^2}\left(\frac{1}{1+\displaystyle \frac{9}{z^2}}\right)$ = $\displaystyle \frac{1}{z^{2}}\left(\sum_{n=0}^{\infty} \left(\frac{9}{z^{2}}\right)^{n}\right) =\sum_{n=0}^{\infty} \frac{9}{z^{2n+2}}$; Para $\displaystyle \frac{9}{|z^{2}|}< 1$ => $|z| >3$ 

---
**Teorema**
Seja $z_0$ um ponto singular isolado da função f. Então as duas afirmações são equivalentes
	1. $z_0$ é um polo de ordem m(m=1,2,3,...)
	2. $f(z)$ pode ser analítica na forma
	$$f(z)=\frac{\phi(z)}{(z-z_0)^m}$$ Onde $\phi(z)$ é analítica e diferente de zero em $z_0$
	 e $\displaystyle Res_{z=z_0}f(z) =\frac{\phi^{(m-1)}(z_0)}{(m-1)!}, \hspace{1cm} onde~~m=2,3,...$  
