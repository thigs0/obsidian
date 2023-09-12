- [[Polinômio de Taylor]] com números complexos
Suponha que a função f esteja na classe de [[Função analítica]] no [[Interior]] de um disco $|Z-Z_0)|< R_0$, centrado no ponto $Z_0$ e com Raio $R_0$ Então f(z) tem uma [[Séries de Potências]] que representa ela.
$$f(z)= \sum_{n=0}^\infty a_n(z-z_0)^n \hspace{2cm} (|z-z_0| < R_0)$$
Onde $$a_n =  \frac{f^{(n)}(z_0)}{n!} \hspace{1cm} (n=0,1,2,...)$$
![[taylor_domain.png|center|400]]

---
Algumas expressões
$\displaystyle \large \frac{1}{1-z} = \sum_{n=0}^\infty z^n = 1+z+z^2+z^3+... \hspace{3cm} (|z|<1)$
	Prova:
	Temos a sequência $1+z+z^2+z^3+...+z^n= S$
	então temos também que $zS =z+z^2+z^3+...+z^{n+1}$ 
	subtraindo uma expressão da outra
	$\begin{matrix}~~~~~~ S = & 1 & +z &+z^2 &+z^3 &+...& +z^n\\ -zS =&& -z&-z^2&-...&...&-z^n&-z^{n+1} \end{matrix}$
	$(1-z)S~=~~1\hspace{6.1cm} -z^{n+1}$ 
	 => $\displaystyle S= \frac{1-z^{n+1}}{1-z}$, Se $|z|<1$ o limite diminui e tende à 0 de forma que
	 $\displaystyle \lim_{n\to \infty} = \frac{1}{1-z}$ 
	 
$\displaystyle \large e^z = \sum_{n=0}^\infty \frac{z^n}{n!}=1+\frac{z}{1!}+\frac{z^2}{2!}+...$
$\displaystyle \large Sin(z) = \sum_{n=0}^\infty (-1)^n \frac{z^{2n+1}}{(2n+1)!} = z- \frac{z^3}{3!}+\frac{z^5}{5!}-....$
	Prova:
	Temos da definição de [[Seno complexo]] que 
	$\displaystyle sinh(z) = \frac{e^{iz}-e^{-iz}}{2} = \frac{e^{iz}}{2}- \frac{e^{-iz}}{2}$ 
	Como conhecemos a série da exponencial, podemos abrir ela
	$\displaystyle \frac{1}{2}\left( \sum_{n=0}^\infty \frac{(iz)^n}{n!}\right) - \frac{1}{2}\left( \sum_{n=0}^\infty \frac{(-iz)^n}{n!}\right) = \frac{1}{2}\left( \sum_{n=0}^n \frac{[i^n-(-i)^n]z^n}{n!}\right)$
	Observamos que nos termos pares, teremos 0 nos couchetes, restando apenas os ímpares
	$\displaystyle \frac{1}{2}\left( \sum_{n=0}^\infty \frac{2i^{2n+1}z^{2n+1}}{(2n+1)!}\right) = \sum_{n=0}^\infty \frac{(iz)^{2n+1}}{(2n+1)!}$ 
$\displaystyle \large Cos(z) = \sum_{n=0}^\infty (-1)^n\frac{z^{2n}}{(2n)!} = 1-\frac{z^2}{2!}+\frac{z^4}{4!}+...$
	Prova:
	Temos que [[Cosseno complexo]] é dado por $\displaystyle Cos(z) = \frac{e^{iz}+e^{-iz}}{2}$, usando a expansão do exponencial
	$\displaystyle Cos(z) = \frac{e^{iz}}{2}+\frac{e^{-iz}}{2}= \frac{1}{2}\sum_{n=0}^\infty \frac{(iz)^n}{n!}+ \frac{1}{2}\sum_{n=0}^\infty \frac{(-iz)^n}{n!} = \frac{1}{2}\sum_{n=0}^\infty \frac{[i^n+(-i)^n]z^n}{n!}$    
$\displaystyle \large Sinh(z) = \sum_{n=0}^\infty \frac{z^{2n+1}}{(2n+1)!}=z+\frac{z^3}{3!}+\frac{z^5}{5!}+...$ 
	Prova:
$\displaystyle \large Cosh(z) = \sum_{n=0}^\infty \frac{z^{2n}}{(2n)!}= 1+\frac{z^2}{2!}+\frac{z^4}{4!}+...$
	Prova:
	Temos que $\displaystyle Cosh(z) = \frac{e^z+e^{-z}}{2}= \frac{e^z}{2}+\frac{e^{-z}}{2}$ e podemos representar $e^z$ em forma de soma infinita
	$\displaystyle Cosh(z) = \frac{1}{2}\sum_{n=0}^\infty \frac{z^n}{n!}+ \frac{1}{2}\sum_{n=0}^\infty \frac{(-z)^n}{n!} = \frac{1}{2}\sum_{n=0}^\infty \frac{[1+(-1)^n]z^n}{n!}$, para n ímpar, o termo no parentesis é 0. De tal forma que representamos apenas os termos pares
	$\displaystyle \frac{1}{2}\sum_{n = 0}^\infty \frac{[1+1]z^{2n}}{(2n)!} = \frac{1}{2}\sum_{n=0}^\infty \frac{2z^{2n}}{(2n)!} =  \sum_{n=0}^\infty \frac{z^{2n}}{(2n)!}~~~\blacksquare$   

---

### Convergência absoluta e uniforme

**Teorema**
Se a série de potência  $\displaystyle \sum_{n=0}^{\infty} a_n(z-z_0)^n$ converge quando $z = z_1$, então é convergente absolutamente para cada ponto no disco aberto $|z-z_0|<R_1$ Onde $R_1=|Z_1-z_0|$


---
**Teorema** 
Seja C qualquer contorno interior de um circulo de convergência de uma série de potência e $g(z)$ denota uma função que é contínua em C. A série formada pela multiplicação de cada termo da série de $g(z)$ pode ser integrada termo a termo sobre C.
$$\int_c g(z)S(z)dz = \sum_{n=0}^{\infty}a_ng(z)(z-z_0)^ndz$$
**Corolário**
A soma de S(z) de uma série de potência é [[Holomorfa]] em cada ponto interior de z no circulo de convergência

**Teorema**
A série de potência pode ser diferenciada termo a termo quando z estiver dentro do circulo de convergência da série
$$S'(z) = \sum_{n=1}^{\infty}na_n (z-z_0)^{n-1}$$
Exemplo:
$\displaystyle -\frac{1}{z} = \sum_{n=0}^{\infty}(-1)^nn(z-1)^{n-1}$    $(|z-1|<1)$
$\displaystyle \frac{1}{z^{2}}= \sum_{n=0}^{\infty}(-1)^n(n+1)(z-1)^{n}$   $(|z-1|<1)$

---
### Multiplicação e divisão
Seja $f(x)~e~g(x)$ funções com representação em série de potência.
$$f(x).g(x) = \sum_{n=0}^\infty c_n(z-z_0)^n$$
tal que usando a [[Regra geral de Leibniz]], obtemos: $\displaystyle c_n = \sum_{k=0}^n \frac{f^{(n)}(z_0)}{k!}.\frac{g^{(n-k)}(z_0)}{(n-k)!}= \sum_{k=0}^n a_kb_{n-k}$  


