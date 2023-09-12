
**Momento**: O momento de ordem n (n-ésimo momento) de uma [[Variável Aleatória]] X, é dado por valor esperado de X elevado a n $E(X^n)$, $n \geq 1$

**Definição** -> A função geradora de momentos (fgm) de X, denotada por M(t), é definida para $t \in \mathbb{R}$ como:
$$M(t) = E(e^{tx})$$
	- Caso discreto:
		$\displaystyle M(t) = E(e^{tx}) = \sum_{x=1}^\infty e^{tx}p(x)$ 
	- Caso [[Contínua]]
		$\displaystyle M(t) = E(e^{tx}) = \int_{-\infty}^\infty e^{tx}fxdx$ 
Observe que
M(t) = $E(e^{tx})$
M'(t) = $\displaystyle \frac{d}{dt}E(e^{tX}) = E\left( \frac{d}{dt}e^{tX} \right) = E(e^{Xt}X)$
M''(t) = $E(e^{Xt}X^2)$
.
.
.
$M^{(n)}(t) = E(e^{Xt}X^n)$ --> Prova por [[Complementos de matemática/Indução]]
Caso apliquemos em t=0, obtemos o valor esperado de $X^n$

*Exemplos*
	(1) X~Bin(n,p)
	M(t) = $E(e^{tx}) = \sum_{x} e^{tx}p(x) = \sum_x e^{tx}\begin{pmatrix}n\\x \end{pmatrix} p^x(1-p)^{n-x}$
	= $\displaystyle \sum_x \begin{pmatrix}n\\x \end{pmatrix} (e^t p)^x (1-p)^{n-x} \xRightarrow {\text{Semelhanças com binômio de Newton}} [e^tp +(1-p)]^n$
	(2) X~N($\mu , \sigma^2$)
	padronizamos em Z
	$M_z(t)$ =$\displaystyle E^{e^{tx}} = \int_{-\infty}^\infty e^{tx}f(x)dx = \int_{-\infty}^\infty e^{tx} \frac{1}{\sqrt{2 \pi}} e^{-x^2/2}dx = \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}} exp\left( tx - \frac{x^2}{2}\right)dx$ 
	$\displaystyle \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}} exp\left( -\frac{x^2 -2tx}{2}\right)dx \xRightarrow {\text{completando quadrado dentro do exponencial}} \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}} exp\left( tx - \frac{x^2-2tx +t^2}{2} \frac{t^2}{2}\right)dx$
	$\displaystyle \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}} exp\left( tx - \frac{-(x-t)^2}{2}+ \frac{t^2}{2}\right)dx = e^{t^2/2} \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}} e^{-\frac{(x-t)^2}{2}}dx = e^{t^2/2} ~N(t,1) = e^{t^2/2}$
	Retornando à variável originária
	e temos $\displaystyle exp\left( t \mu + \frac{(t\mu)^2}{2}\right)$

**Tabela com fgm**
| **Distribuição**      | **Fgm**                                                    |
| ----------------- | ------------------------------------------------------- |
| Poisson           | $exp\left( \lambda (e^t-1)\right)$                      |
| Geométrica        | ($pe^T$)/($1-(1-p)e^t$)                                 |
| Binomial negativa | $\displaystyle \left[ \frac{p2^t}{1-(1-p)e^t}\right]^r$ |
| Uniforme          | $\displaystyle \large\frac{e^{bt}-e^{at}}{t(b-a)}$                          |
| Exponencial       | $\displaystyle \frac{\lambda}{\lambda -t}$                            |
| Gama              | $\displaystyle \left(\frac{\lambda}{\lambda -t} \right)^\alpha$                                                        |

**Propriedades**
1) A fgm determina unicamente a distribuição de X 
	Exemplo: Se a fgm de X é $M(t) = exp(e^t-1)$ -> X~Poisson(5)
2) Se X tem fgm $M_x(t)$, então Y=aX+b tem fgm dada por 
$$\large M_Y(t) = e^{bt}M_X(at)$$
3) Se X e Y são independentes e Z = X+Y, então: 
$$M_Z(t) = M_X(t).M_Y(t)$$

_Exemplo_:
X~N($\mu_1, \sigma_1^2$), Y ~N($\mu_2, \sigma_2^2$) -> Z= X+Y ?
$\displaystyle M_z(t) = M_x(t)M_y(t) = exp\left( \frac{\sigma_1^2 t^2}{2}+ \mu_1 t \right) exp\left( \frac{\mu_2^1 t^2}{2}+ \mu_2t\right) = exp\left( \frac{\sigma_1^2t^2}{2}+ \mu_1t+ \frac{\sigma_2^2t^2}{2}+ \mu_2t\right)$
= $\displaystyle exp\left( \frac{(\sigma_1^2 + \sigma_2^2)t}{2}+ (\mu_1+\mu_2)t\right)\rightarrow Z= X+Y= N(\mu_1+\mu_2, \sigma_1^2+\sigma_2^2)$