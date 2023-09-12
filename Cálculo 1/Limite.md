Foi desenvolvido por **Augustin-Louis Cauchy** e **Karl W.T Weiertrass**, Limite de uma [[função]] f(x) é quando x se aproxima de a
- O valor que tende em um ponto, mas não no ponto

***Definição de limite***
$$\forall \epsilon>0,\exists\delta>0~~~tq~0<|x-a|<\epsilon\Rightarrow |f(x)-L|<\epsilon$$

**Proposições**
- $\lim_{x\to a}c=c$
- $\lim_{x\to a}x=a$
- Se $\lim_{x\to a}f(x)=L$ e $\lim_{x\to a}g(x)=M$
- $\lim_{x\to a}(f+g)(x)=L+M$
- $\lim_{x\to a}(f.g)(x)=LM$
- $\lim_{x\to a}\frac{f}{g}(x)=\frac{L}{M}$


**[[Limite fundamental da trigonometria]]**

```functionplot
---
title: Gráfico do limite Fundamental da trigonometria
disableZoom: false
bounds: [-12, 12, -2, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = sin(x)/x

```
**Propriedades de limite**
1. Constante dentro do limite
	$\displaystyle \lim_{x\to b} k f(x) ~~=~~ k \lim_{x \to b} f(x)$
2. [[Limite da soma]]
	$\lim_{x \to b} (f(x)+f(b))~~=~~\lim_{x \to b} f(x) +\lim_{x \to b}f(b)$ 

- ##### [[L'Hôpital]]
	Caso o limite fique indeterminado, podemos derivar ambos os termos e o resultado do limite permanece	$$\lim_{x\to0} \frac{f'(x)}{g'(x)} = \lim_{x\to 0} \frac{f(x)}{g(x)}$$
	Prova:
	![[Regras_L_Hospital.pdf|200]] 
	
