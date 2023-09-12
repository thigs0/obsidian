*Caso discreto*
| x      | -2  | -1  | 0   | 1   | 2   |
| ------ | --- | --- | --- | --- | --- |
| P(X=x) | 0.1 | 0.1 | 0.2 | 0.3 | 0.3 |

Qual é a fdp de Y = $x^2$, que é uma [[Variável Aleatória]]
P(Y=0) = P(X=0) = 0.2
P(Y=1) = P(X=-1 ou X=1) = 0.4
P(Y=4) = P(X=-2 ou X=2) = 0.4
Com isto, temos
| y   | P(Y=y) |
| --- | ------ |
| 0   | 0.2    |
| 1   | 0.4    |
| 4   | 0.4       |


*Caso contínuo*
X ~ Uni(0, 1) , Y = $X^2$ ?

$F_y(y) = P(Y \leq y) = P(X^2 \leq y) \xRightarrow {\text{Ser invertível no intervalo dado}} P(X \leq \sqrt{y}) = F_x(\sqrt{y})= \sqrt{y}$ 
$\displaystyle f_y(y) = F_y'(y) = (\sqrt{y})' = \frac{y^{-1/2}}{2} = \frac{1}{2 \sqrt{y}} \mathbb{I}_{[0,1]}^{(y)}$

**Proposição**
	Seja X uma [[Variáveis aleatórias contínua]] com fdp $f_X$. Suponha que g(x) seja uma [[função monôtona]] e derivável. Então a variável aleatória tem fdp dada por: $$f_Y(y) = f_X(g^{-1}(y))\left| \frac{d g^{-1}(y)}{dy}\right|, ~~y=g(x)~~~~ \text{para algum x}$$
	**Demonstração**
	Suponha que g(x) é crescente e Y = g(x)
	$F_y(y) = P(Y \leq y) = P(g(x) \leq y) = P(X \leq g^(-1)(y)) = F_X(g^{-1}(y))$
	$\displaystyle f_Y(y) = F_Y'(y) = (F_X(g^{-1}(y)))' \xRightarrow {\text{regra da cadeia}} f_X(g^{-1}(y)). \frac{d}{dy} g^{-1}(y).$  $\blacksquare$ 