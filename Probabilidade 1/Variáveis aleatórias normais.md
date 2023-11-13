É da forma $$\displaystyle \Large f(x) =\frac{1}{\sqrt{2\pi}\sigma}e^{-(x-\mu)^2/2\sigma^2}$$
```functionplot
---
title: Curva Normal
disableZoom: false
bounds: [-4, 4, 0, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = (2.1415^(-x^2/2))

```
$\displaystyle \large \mu$ é o valor central da curva, linha de simetria
$\displaystyle \large \sigma$ é a variabilidade 

A curva também é dada pela [[EDO]]
$y' = 2yx$ 

**Valor esperado**
	$E(x) = \mu$
**Variância**
	$Var(x) = \sigma^2$ 

X ~ N($\mu, \sigma^2$)

Caso N(0, 1) -> Chamamos de curva normal padrão. Ela é importante por sempre podermos transformar um problema variado em uma normal padrão; em um processo chamado padronização
$$Z = \frac{x-\mu}{\sigma},~~Z-N(0,1)$$
_Exemplo_
	$\displaystyle P(x \leq a) = P(\frac{x-\mu}{\sigma}\leq \frac{a -\mu}{\sigma}) = P(Z\leq \frac{a-\mu}{\sigma})=\phi(\frac{a-\mu}{\sigma})$ 

Se fizermos uma função linear de uma distribuição normal, ela também terá distribuição normal
$Y = aX+b$ ~ $N(a \mu +b, a^2b^2)$

**Proposição**
(1) Padronização
	Se X ~ $\displaystyle N(\mu , \sigma^2) \Rightarrow Z = \frac{X-\mu}{\sigma}$ ~ N(0, 1)
(2) 
	$\displaystyle var(Z) = E(Z^2) - 0 = E(Z^2) = \int_{-\infty}^\infty x^2 \frac{1}{\sqrt{2\pi}}e^{-x^2/2}$
	$\displaystyle \large \xRightarrow[u=x, du=dx]{dv = xe^{-x^2/2, v -e^{-x^2/2}}}\left[ -xe^{-x^2/2}|_{-\infty}^\infty + \int_{-\infty}^\infty e^{-x^2/2}dx\right]\frac{1}{\sqrt{2 \pi}} = \frac{-1}{\sqrt{2 \pi}}xe^{-x^2/2}|_{-\infty}^\infty + \int_{-\infty}^\infty \frac{1}{\sqrt{2 \pi}}e^{-x^2/2}dx = 1$ 
	Logo:
	$\displaystyle Var(x) = var(\sigma Z+\mu) = \sigma^2 Var(Z) = \sigma^2$
(3) Notação
	N(0, 1): distribuição normal
	$\phi(x) = \frac{1}{\sqrt{2 \pi}} e^{-x^2/2} \mathbb{I}_{\mathbb{R}}^{(x)}$
	$\phi (x) = F(x) = \int_{-\infty}^\infty \phi(t)dt$


 **Tabela da aculmulada**
 Linhas -> Primeiro dígito importante
 Coluna -> Segundo dígito importante

**Aproximação normal para [[Distribuição binomial]]**
	Se X--Bin(n, p) para n suficientemente grande, temos 
	X $\approx N(np, np(1-p))$
	**Critérios**
	Ross: np(1-p) $\leq 10$

**Exemplo:**
	X: # de ingressantes em um grupo de 450 matrículas
	p = 0.3 
	P(X > 150)
	X ~ Bin(450, 0.3)
	P(X > 150) $= \sum_{x=151}^450 \begin{pmatrix} 450 \\ x\end{pmatrix} 0.3^x 0.7^{450-x}$
	Pela aproximação normal (Com correção de continuidade):
	$P(X>150) = P(X\geq 150.5)$

**Aproximação para a [[Distribuição de Poisson]]**