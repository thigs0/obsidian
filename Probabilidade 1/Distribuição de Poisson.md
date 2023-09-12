Caso tenhamos um número de contagens que aproximem infinito

**Def:**
	Uma variável aleatória X tem distribuição de Poisson com parâmetro $\large \lambda >0$ se sua [[Função de probabilidade]] é da forma:
		$\displaystyle \large p(x)= P(X=x)= \frac{\lambda^x e^{-\lambda}}{x!}\mathbb{I}_{\{0,...., \infty\}}^{(x)}$
	e escrevemos X ~ Poisson($\lambda$)
```functionplot
---
title: 
disableZoom: false
bounds: [1, 4, 1.3, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = (1^x* 2.1415^(-1))/1

```


São do tipo:
- O número de clientes que entram em uma agência num certo dia.
- O número de partículas emitidas por uma fonte radioativa em um período fixo de tempo


*Exemplos*
	(1) X: # de partículas emitidas em 1 segundo por grama de um material radioativo
	Sabe-se que $\lambda$ = 3.2. Qual a probabilidade de não mais do que 2 partículas sejam emitidas?
	X ~ Poisson(3.2)
	P(x) = $\displaystyle \frac{3.2^xe^{(-3.2)}}{x!}$

**Valor esperado**
	E(x) = $\displaystyle \sum_0^\infty xp(x) = \sum_{x=0}^\infty x \frac{\lambda^xe^{-\lambda}}{x!} = \sum_{x=1}^\infty x \frac{\lambda^xe^{-\lambda}}{x!} = \lambda\sum_{x=1}^\infty x \frac{\lambda^{x-1}e^{-\lambda}}{x!} =\lambda\sum_{x=1}^\infty  \frac{\lambda^{x-1}e^{-\lambda}}{(x-1)!}$
	$\displaystyle \xRightarrow {y=x-1} \lambda \sum_{y=0}^\infty \frac{\lambda^y e^{-\lambda}}{y!} \xRightarrow{\text{A soma é um por aproximação de Taylor}} \lambda$

**Variancia**
	Var(x) = $\lambda$ 

**Propriedades**
	1) Dado X ~Poisson($\lambda_1$) e Y ~ Poisson($\lambda_2$) Independentes<-> X+Y ~ Poisson($\lambda_1+ \lambda_2$)
		Prova:
		P(X+Y+n) = $\displaystyle \sum_{k=0}^n p(X=k, Y=n-k) \xRightarrow{\text{São independentes}}  \sum_{k=0}^n p(X=k).p(Y=n-k)$
		$\large \displaystyle \sum_{k=0}^n \frac{\lambda_1^ke^{\lambda_1}}{k!}.\frac{\lambda_2^{n-k}e^{-\lambda_2}}{(n-k)!} = \frac{1}{n!}\sum_{k=0}^n \frac{n!}{k!(n-k)!}e^{-(\lambda_1+\lambda_2)}.\lambda_1^k. \lambda_2^{n-k}$
		$\large \displaystyle \frac{e^{-(\lambda_1+\lambda_2)}}{n!}\sum_{k=0}^n \begin{pmatrix}n \\k \end{pmatrix} \lambda_1^k \lambda_2^{n-k} = \frac{(\lambda_1+\lambda_2)e^{-(\lambda_1+\lambda_2)}}{n!} = Poisson(\lambda_1+\lambda_2)$

