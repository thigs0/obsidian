Temos $\displaystyle \sum_{i=0}^\infty a_i$

Definimos a série infinita como
	$\displaystyle \lim_{n\to \infty} \sum_{i=0}^\infty a_i$ 

**[[Série geométrica]]**
A forma geral da série geométrica é dada por
	$\displaystyle \sum_{k=1}^\infty x^k$; Para resolvá-la termos
	$S_n = x+x^2+x^3+...+x^n$ e construímos
	$xS_n = x^2+x^3+x^4+...+x^{n+1}$ e subtraímos as duas
	$S_n-xS_n = x-x^{n+1}$ -> $\displaystyle S_n = \frac{x-x^{n+1}}{(1-x)}$ para $x \neq 0$ 
	e tomamos o [[Limite]]
	$\displaystyle \lim_{n \to \infty} \frac{x-x^{n+1}}{(1-x)}$  $\displaystyle \begin{cases} \frac{x}{1-x} ~~~Se~~|x|<1\\-\infty ~~~Se~~|x|>1\end{cases}$
**[[Série P]]**
	Essas séries são da forma
	$\displaystyle \sum_{k=1}^\infty \frac{1}{K^p}~~|k \in \mathbb{R}$ 
	Se  $p\leq1$ a série diverge
	Se p> 1 a série converge
	Prova usa [[Teste da integral]]

**Teorema**
		Se a série converge, então, o limite dos termos da série é 0. A volta não é válida
		$\lim_{n \to \infty} (S_n-S_{n-1}) = S-S =0$ e o termo da subtração dos S é justamente $a_n$ 
		**Usamos mais a contra-positiva** 
