É usada em casos que adquirem valores 0 ou 1, sucesso e fracasso.
Considere a V.A X dada por:
$\displaystyle X \large \begin{cases} 1, \text{ com probabilidade p} \\ 0, \text{ com probabilidade 1-p}\end{cases}$; Podemos escrever a fp de x como:
p(x) = P(X=x)= $\displaystyle p^x(1-p)^{1-x}; ~~x=0,1$

```functionplot
---
title: 
disableZoom: false
bounds: [-1, 4, -1, 4]
grid: true
xLabel: x
yLabel: y
---

f(x) = ((0.5)^x)*(1-0.5)^(1-x)

```
Dizemos que X tem distribuição de Bernouli com parâmetro p e escrevemos X ~ ber(p)
$E(x) = p$
E($x^2$) = $\displaystyle \sum_x x^2p(x) = 0^2(1-p) +1^2.p = p$
Var(x) = $E(x^2)-E(x^~2) = p-(p^2)= p(1-p)$

**Obs(Função indicadora)**:
p(x) = $p^x(1-p)^{1-x}$, x = 0 ou 1
p(x) = $\displaystyle \large p^x (1-p)^{1-x} \mathbb{I}_{\{0,1\}}^{(x)}$, em que $\mathbb{I}_A^{(x)} = \begin{cases} 1, ~~Se ~~x \in A \\ 0, ~~ \text{Se caso contrário} \end{cases}$([[Função indicadora]])
_Exemplo_:
	$\displaystyle \large P(1) = p^1 (1-p)^{1-1}\large  \mathbb{I}_{\{0,1\}}^{(1)} = p$
	$\large \epsilon$: Retirar uma peça de um lote
	$X = \begin{cases} 1, \text{ Se a peça é defeituosa}\\ 0, \text{ Caso contrário}\end{cases}$; Suponha que p = 0.1
	Então, X ~ Ber(0.1)
	P(x) = $0.1^x(1-0.1)^{1-x} \mathbb{I}_{\{0,1\}}^{(x)}$
	E(x) = 0.1
	var(X) = 0.1(1-0.1) = 0.09

