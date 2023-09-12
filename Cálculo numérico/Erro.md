- Erro de conversão
O computador usa a base [[Binário]] e a conversão da base decimal para binária deixa os números em forma aproximada

- ### Erro absoluto
	$E_{ABS(\hat x)} = |x-\hat x|$; em que x é o valor exato e $\hat x$ é a aproximação

- ### Erro relativo
	$E_{Rel}(\hat x) =\frac{|x-\hat x|}{|\hat x|} = \frac{E_{ABS}}{|X|}$

- ### Erro adimensional
	$\displaystyle E_{ADM} = \frac{|x-\hat x|}{L}$ ; Em que L é uma grandeza característica do sistema

- ### Erro em operações
	Supondo que o número verdadeiro possa ser escrito como $\displaystyle x = \bar{x} + E_x$
	Então o erro de x + y é :
	$$E_{x+y} = E_x + E_y;~~absoluto$$
	$$E_{x+y}= E_x \left( \frac{\bar{x}}{\bar{x}+ \bar{y}} \right) + E_y \left( \frac{\bar{y}}{\bar{x}+ \bar{y}} \right); ~~ Relativo$$
	erro de x.y é:
	$$\displaystyle E_{xy} = \bar{x} \bar{y}+\bar{x} E_y + \bar{y} E_x + E_xE_y; ~~absoluto$$
	$$E_{xy} = E_x + X_y;~~Relativo$$

## Unidade de arredondamento
#### Algoritmos
==Pseudo-algoritmo==
	u <- 1
	Enquanto 1+u >1
		u <-- u/2
	mostre (u*2)
	
```octave
u=1
while 1+u>1
u=u/2
endwhile
disp(2*u)
```
