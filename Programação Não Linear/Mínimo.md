$f:\mathbb{R}^n\to \mathbb{R}~~and~~f\in c^0$ e uma superfície $S \subset \mathbb{R}^n$ 
-> $\min f(x); x \in S$ 

- mínimo e máximo
	**Definição**
	Se a função está restrita ao conjunto s, se existe um $x^*$ tal que $\forall x\in S, f(x^*)\leq f(x)$, Então chamamos $x^*$ de minimizador e $f(x^*)$ mínimo da função
	**Definição** **[[Minimizador]]**
	$x^*\in S$ é um minimizador global de $f:\mathbb{R}^n\to \mathbb{R}$ em S se $f(x^*)\leq f(x)$ para todo $x\in S$ 
	**Definição** **[[Mínimo local]]**
	$x^{*}\in S$ é um minimizador local de $f:\mathbb{R}^{n}\to \mathbb{R}$ em S se existe $\epsilon>0$ tal que $f(x^*)\leq f(x)$ para todo $x\in \{x\in S| \|x-x^*\|<\epsilon\}$ 
	**Definição** 
**Teorema**
	Dado uma [[função]] contínua, o mínimo dela é igual ao mínimo do negativo da função
	$\displaystyle \min_{x\in S} \{f(x)\}=-\displaystyle \max_{x\in S}\{-f(x)\}$
	

```functionplot
---
title: Função f
disableZoom: false
bounds: [2, 12, -4, 5]
grid: true
xLabel: x
yLabel: y
---

f(x) = sin(x)*log(x)

```


- Avaliamos os pontos que apresentam mínimo e máximo
	- $x_1,x_2,x_3,x_4x...$ 

Se modificarmos a função, de forma que fique
```functionplot
---
title: Função f
disableZoom: false
bounds: [2, 12, -4, 5]
grid: true
xLabel: x
yLabel: y
---

f(x) = sin(x)*log(x)/(1.2^x)

```


**Teorema**
Todo minimizador global é minimizador local

