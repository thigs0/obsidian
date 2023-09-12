### [[Singularidade Isolada]]
Se uma função é analítica em todos os pontos, mas falha em ser [[Holomorfa]] apenas no ponto $z_0$, de modo que é sempre podemos escolher um $\epsilon$ de forma que a função dentro de um disco furado tenha apenas $z_0$ como singularidade


**Exemplo**
A função $$f(z)= \frac{1}{\sin(\pi/z)}$$
Cujo gráfico real é 
```functionplot
---
title: Gráfico da função 1 sobre seno(pi/x)
disableZoom: false
bounds: [-1, 1, 2, -2]
grid: true
xLabel: x
yLabel: y
---

f(x) = 1/(sin(PI/x))

```
E o gráfico complexo é:
![[UmSobreSenoComplexo.png|center|500]]
Não há [[Derivada]] em z=0, sendo que $\sin(\pi /z)=0$, temos também que nos pontos $z=1/n \hspace{1cm} (n=\pm1,\pm2,\pm3,...)$ a derivada não existe.
Para todo $\epsilon>0$ Temos que $m=1/\epsilon$ também é um ponto isolado. Assim, não existe ponto isolado na função acima 

**Singularidades**
Podem ser divididos em 3 tipos
- Removíveis
	$b_k=0, \forall k \in \mathbb{N}$
	Perceba que o [[Resíduos]] de uma [[Singularidade removível]] é 0
- Pólos
	- ordem 1
		$b_1 \neq 0$, e $b_k =0, k>1$ 
	- ordem 2
		$b_2 \neq 0$, e $b_k =0, k>2$
	- ordem 3
		$b_2 \neq 0,$ e $b_k=0, k>2$
	- ...
- Essenciais
	$\forall k \in \mathbb{R}, \exists n>k;~se~b_k=0,b_n=0$

---
**Exemplos**
A função $$f(z)=\frac{1-\cosh(z)}{z^2}$$
Quando separamos em $\displaystyle f(z)= \frac{1}{z^2}(1-\cosh(z))$ e expandimos o segundo termo como uma [[Séries de Potências]].
$\displaystyle f(z)=\frac{1}{z^2}\left[1-\left(1+\frac{z^2}{2!}+\frac{z^4}{4!}+\frac{z^6}{6!}+\right)\right]=-\frac{1}{2!}-\frac{z^2}{4!}-\frac{z^4}{6!}-...$ 
Então a singularidade removível.

