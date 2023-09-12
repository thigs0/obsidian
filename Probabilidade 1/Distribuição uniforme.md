Dizemos que X tem distribuição uniforme no intervalo [a, b], se sua função densidade de probabilidade é dada por:
		f(x) = $\displaystyle \large \begin{cases} \frac{1}{b-a}, ~a \leq x \leq b \\ 0, ~c.c\end{cases}$
		E escrevemos X ~U[a,b] , em que a e b são parâmetros
		(1) F(x) = $\displaystyle \int_{-\infty}^\infty f(t)dt \xrightarrow{a \leq x \leq b} \int_1^x \frac{1}{b-a}dt= \frac{1}{b-a}.t|_a^x = \frac{x-a}{b-a}$
		Logo:
		$\displaystyle F(x) = \begin{cases} 0, ~x<a\\ \frac{x-a}{b-a}, a \leq x \leq b\\ 1, x>b\end{cases}$

**Valor esperado**
	$\displaystyle E(x) = \int_a^b x.\frac{1}{b-a}dx = \frac{1}{b-a}.\frac{x^2}{2}|_a^b = \frac{b^2-a^1}{2(b-a)}= \frac{b+a}{2}$
	e esta é a esperança

**Variância** 
		É dada por $\displaystyle Var(X) = \frac{(b-a)^2}{12}$

_Exemplo_
	X: Posição de vazamento de um tubo de 6 metros
	X~U(0, 6)
	Queremos $P(0<x<1 ~ou~ 5\leq x \leq 6)$  P(0<x<1) + P(5<x<6) = $\displaystyle \int_0^1 \frac{1}{6}dx + \int_5^6 \frac{1}{6}dx = \frac{1}{3}$
