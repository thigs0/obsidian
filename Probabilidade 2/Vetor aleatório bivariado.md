Seja $\lambda=(x_1,x_2)$ um [[Vetor]] aleatório, onde $x_1$ e $x_2$ são [[Variáveis aleatórias contínua]]
1) Caso discreto: Neste caso as componentes de X são v.a discretas
$$R_x=\left\{ (x_1,x_2)\in \mathbb{R}^2: x_1\in \mathbb{R}~e~x_2\in\mathbb{R} \right\}~~~\text{conjunto de todos os possíveis valores de x}$$
a fdp conjunta de $x_1$ e $x_2$ ou simplesmente de X é definida por
$$P_x(x)=P(X_1=x_1,X_2=x_2)$$
que satisfaz
	1) $P_x(X)\geq 0$
	2) $\sum\limits_x P_x(x)=\sum\limits_{x_1} \sum\limits_{x_2} P(X_1=x_1,X_2=x_2)=1$ 
**Exemplo**

| X\Y | 0   | 1   | 2   |
| --- | --- | --- | --- |
| 0   | 1/4 | 0   | 1/4 |
| 1   | 0   | 1/2 | 0    |
A [[Distribuição marginal]] da fdp é
$P(X_1=x_i)=\sum\limits_j P(X_1=x_i,x_2=y_j)$
$P(X_2=y_j)=\sum\limits_i P(X_1=x_i,X_2=y_j)$
para ser independente, temos que as probabilidades marginais multiplicadas resultam no valor central

2) Caso contínuo: Dizemos que o vetor (x,y) é absolutamente contínuo se existir uma função $f(x,y) t.q$
	1) $f(x,y)\geq0$
	2) $\int_{-\infty}^\infty \int_{-\infty}^\infty f(x,y)dxdy=1$
**Exemplo**
Sejam X e Y variáveis aleatórias
$$f(x,y)=\begin{cases} 3e^{-3x-y}~~x>0,y>0 \\0\end{cases}$$

**Definição**
Dizemos que $X_1,X_2,...,X_n$ são [[Variáveis aleatórias contínua]] independentes e identicamente distribuidos (iid) se
1) $X_1,...,X_n$ são v.a independentes
2) $X_1,...,X_n$ têm as mesmas distribuições
Exemplos
