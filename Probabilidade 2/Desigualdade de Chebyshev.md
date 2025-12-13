Se X é uma [[Variável Aleatória]] com média finita $\mu$ e variância $\sigma^2$, então, para qualquer valor $k>0$
$$P(|X-\mu|\geq k)\leq \frac{\sigma^2}{k^2}$$
**demonstração**
Como $(X-\mu)^2 \geq 0$, aplicamos a [[Desigualdade de Markov]]
$\displaystyle P( (X-\mu)^2\geq k^2)\leq k^2)\leq \frac{\sigma^2}{k^2}$ , como $(X-\mu)^2 \leq k^2 \Leftrightarrow |X-\mu|\leq k$ então
$\displaystyle P(|X-\mu|\geq k)\leq \frac{\mathbb{E}[(X-\mu)^2]}{k^2}=\frac{\sigma^2}{k^2}$

**Exemplo**
Suponha que se saiba que o número de itens produzidos por uma fábrica durante uma semana seja uma variável aleatória com média $\mu=50$
1. Se é sabido que a variância da produção de uma semana é igual a 25. Então o que se pode dizer sobre a probabilidade de que a produção desta semana esteja entre 40 e 60?
Pela desigualdade de Chebyshev,
$P(|X-50|\geq 10)\leq 1-\frac{1}{4}=\frac{3}{4}$
