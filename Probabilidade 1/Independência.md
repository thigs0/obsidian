A [[Variável Aleatória]] X e Y são independentes se, para quaisquer [[Conjuntos]] $A, B \in \mathbb{R}$,
$$P(X \in A, Y \in B) = P(X \in A).P(Y \in B)$$
**Obs:** Se X e Y são variáveis discretas, a condição de independência é equivalente a:$$\large p(x,y) = p_Y(x)p_Y(y),~~ \forall x,y \in \mathbb{R}$$
A conjunta é igual ao produto das marginais

_Exemplo_:

| x\y      | $\pi /2$ | $\pi$ | $P_X(x)$ |
| -------- | -------- | ----- | -------- |
| 0        | 0.2      | 0.1   |      0.3    |
| 1        | 0.4      | 0.3   |     0.7     |
| $P_Y(y)$ | 0.6      | 0.4   |  1        |

$\displaystyle \large p\left(0, \frac{\pi}{2}\right) = 0.2. ~~p_X(x).p_Y(\pi/2) = (0.3).(0.6)=0.18$, logo, X e Y não são independentes

**Propriedades**
1) Se X e Y são independentes -> E(g(x).h(y)) = E(g(x)).E(h(y))
	em particular: $E(XY)= E(X)E(Y)$
2) Se X e Y são independentes -> $Var(X+Y) = Var(X)+Var(Y)$
