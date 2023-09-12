**Definição**
	Sejam X e Y [[Variável Aleatória]]
s discretas. A função de probabilidade conjunta de X e Y é dada por:
$$p(x,y) = P(X=x, ~Y=y)$$

*Exemplo*:
	$\large \epsilon$: Lançamento de 2 moedas honestas
	$\Omega$ = $\{(c,c), (c,\bar c), (\bar c, c), (\bar c , \bar c)\}$
	$X = \begin{cases} 1, ~~se~~\omega_1 =C \\ 0, ~~\text{Caso contrário}\end{cases}; ~~~~Y = \begin{cases} 1, ~~se~~\omega_2 =C\\ 0, ~~ \text{caso contrário}\end{cases}$
	$\begin{pmatrix} X \\Y\end{pmatrix}, ~~~\mathscr{X}=\{(0,0), (0,1), (1,0),(1,1)\}$
**Propriedades**
1) p(x,y)$\geq 0$ $\forall (x,y) \in \mathbb{R}^2$
2) $\displaystyle \sum_x \sum_yp(x,y)=1$
3) $\displaystyle p_X(x) = \sum_y p(x,y)$ , $\displaystyle p_Y(y) = \sum_x p(x,y)$
	São chamadas de [[Função de probabilidade marginal]]
	
**Proposição** (Valor esperado): Se X e Y possuem fdp conjunta p(x,y), então; em que g é a função real de duas variáveis dada:
$$E(g(X,Y)) = \sum_x \sum_y cos(x,y)p(x,y)$$
*Exemplo*
| x\y      | $\pi /2$ | $\pi$ | $P_X(x)$ |
| -------- | -------- | ----- | -------- |
| 0        | 0.2      | 0.1   |      0.3    |
| 1        | 0.4      | 0.3   |     0.7     |
| $P_Y(y)$ | 0.6      | 0.4   |  1        |
$\displaystyle E(cos(X,Y)) = \sum_x \sum_y cos(x,y).p(x,y) = 0$
**Obs:** Note que se g(X,Y) = $X \pm Y$, temos que 
$$E(E \pm Y) = E(X) \pm E(Y)$$

