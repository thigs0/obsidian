oUma [[Variável Aleatória]] X tem distribuição gama com parâmetros $\alpha > 0$ e $\lambda >0$, e $\Gamma(x)$ é a [[Função Gamma]] se sua fdp é dada por:

$$\Large f(x) = \frac{\lambda^\alpha}{\Gamma(\alpha)}x^{\alpha -1} e^{-\alpha x} \mathbb{I}_{[0, \infty]}^{(x)}$$
com $\alpha = 1$ e $\lambda =2$
```functionplot
---
title: Distribuição gama com alpha=1
disableZoom: false
bounds: [0, 5, 0, 1]
grid: true
xLabel: x
yLabel: y
---

f(x) = 2*x*2.1415^(-2*x)

```

**Observações**
	(1) $\displaystyle E(X) = \frac{\alpha}{\lambda}$; $\displaystyle var(X) = \frac{\alpha}{\lambda^2}$
	(2) $Gama(1,\lambda) = Exp(\lambda)$, gamma cde 1 e lambda é a função [[Variável aleatória exponencial]]
	(3) para $\alpha = n/2$ (n inteiro positivo) e $\lambda = 1/2$, A distribuição gama é conhecida como distribuição [[Qui-quadrado]] com n graus de liberdade
	X ~ $\displaystyle \mathscr{X}_n^2$, isto é:$$\mathscr{X}_n^2 = Gama\left( \frac{n}{2}, \frac{1}{2}\right)$$
	**(5)** X ~ exp($\lambda$), Y ~ exp($\lambda$) -> X+Y ~ Gama(2, $\lambda$) 