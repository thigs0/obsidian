- É mais robusta que a [[Função geradora de momento]]
- Está definida para qualquer distribuição
- Envolve a manipulação de [[Números complexos]]
- quando for [[Absolutamente contínua]] com a densidade f, sua função característica é a simplesmente a [[Transformada de Fourier]] da função da f

A função característica de uma [[Variável Aleatória]] X, denotada por $\varphi_X$, é a [[função]] $\varphi_X:\mathbb{R}\to \mathbb{C}$, definida como
$$\varphi_X(t)=\mathbb{E}[e^{itx}]=\mathbb{E}[cos(tX)]+i\mathbb{E}[sen(tX)],~~~~t\in\mathbb{R}$$
[[Teorema da Unicidade da função característica]]
Se duas variáveis têm a mesma função característica, então têm a mesma distribuição.

**[[Teorema da continuidade de Lévy]]**
Sejam $X$ e $(X_n)_{n\in\mathbb{N}}$ variáveis aleatórias. Então $X_n$ converge em distribuição para X se e somente se $\varphi_{X_n}(t)\to \varphi_X(t)$ para todo $t\in\mathbb{R}$

**Proposição**
Para todo $t\in\mathbb{R}$, vale $|\varphi_X(t)|\leq 1$. Além disso, $\varphi(0)=1$. Ademais, $\varphi_{aX+b}(t)=e^{itb}\varphi_X(at)$ para $a,b\in \mathbb{R}$
**Demonstração**
$|\varphi_X(t)|=|\mathbb{E}[e^{itX}]|\leq \mathbb{E}[e^{tX}]=\mathbb{E}[sen^2(tX)+cos^2(tX)]=1$

**Proposição**
Se $X$ e $Y$ são independentes, então $\varphi_{X+Y}(t)=\varphi_X(t) \cdot \varphi_Y(t)$
**Demonstração**
$\varphi_{X+Y}(t)=\mathbb{E}[e^{it(X+Y)}]=\mathbb{E}[e^{itX}e^{itY}]=\varphi_X(t)\cdot \varphi_Y(t)$

| **Distribuição**                                | $\varphi$                                      |
| ----------------------------------------------- | ---------------------------------------------- |
| [[Distribuição uniforme]] ~ $U(a,b)$            | $\displaystyle\frac{e^{itb}-e^{itb}}{it(b-a)}$ |
| [[Distribuição de Poisson]] ~ $Poison(\lambda)$ | $e^{\lambda(e^{it}-1)}$                        |
| [[Distribuição geométrica]] ~ $Geom(p)$         | $\displaystyle \frac{p}{e^{-it}+p-1}$          |
|                                                 |                                                |

