- Assumem valores em um conjunto não enumerável
- Tempo, temperatura, altura, peso

**Definição**:
	Variável [[Contínua]] X é contínua se existir uma função f(x) $\geq 0,~\forall x \in \mathbb{R}$, tal que P($X \in B$)= $\displaystyle \int_B f(x)dx$ 

(1) f é chamada de função densidade de probabilidade
(2) B= [a, b]
(3) $\displaystyle P(X \in B) = P(a \leq x \leq b) = \int_a^b f(x)dx$
(4) P($a \leq X \leq b$) = P($a < X \leq b$) = P($a \leq X < b$) = P($a< X<b$)
(5) $\displaystyle \int_{-\infty}^\infty f(x)dx = 1$
(6) 
(7) (Valor esperado) 
	$\displaystyle E(x) = \int_{-\infty}^\infty x f(x)dx$
	$\displaystyle E(g(x)) = \int_{-\infty}^\infty g(x)f(x)dx$; para qualquer g(x)

_Exemplo_
	X é uma variável aleatória contínua com a seguinte fdp
	$\displaystyle f(x) = \begin{cases} 1, ~0 \leq x \leq 1\\ 0, ~~c.c\end{cases}=~\mathbb{I}_{[0,1]}^{(x)}$
	Para o intervalo 1/4 e 1/2 é a $\displaystyle \int_{1/4}^{1/2} f(x)dx= 1/4$
.
	Para calcularmos a aculmulada temos:
	$f(x) \begin{cases} 0, se ~x<0\\ x, ~0 \leq x \leq 1\\ 1, ~ x \geq 1 \end{cases}$
	E(x) = $\displaystyle \int_{-\infty}^\infty x f(x)dx = \int_0^1 x.1.dx = \frac{x^2}{2}|_0^1= \frac{1}{2}$
	E(x²) = $\displaystyle \int_{-\infty}^\infty x^2 f(x)= \int_0^1 x^2 .1.dx = \frac{x^3}{3}|_0^1 = \frac{1}{3}$
	Logo: Var(X) = $\displaystyle E(x^2) - E^2(x) = 1/3 - (1/2)^ = \frac{1}{12}$ 
.
	(2) X é variável contínua com fdp 
	$\displaystyle \large  f(x) = \begin{cases} C.(4x-2x^2), ~0 \leq x \leq 2 =~ C(4x-2x^2) \mathbb{I} _{[0,2]}^{(x)} \\ 0, ~c.c\end{cases}$ 
	Antes de calcular, encontramos o valor da constante C. 
	$\displaystyle \int_{-\infty}^\infty f(x)dx =1 \Rightarrow \int_0^2 C(4x-2x^2)dx =1 \Rightarrow C \int_0^2 4xdx - 2C\int_0^2 x^2dx = C\frac{8}{3}$ -> $\displaystyle C= \frac{3}{8}$  
	Substituindo C e calculando temos: P(X>1) = 1/2