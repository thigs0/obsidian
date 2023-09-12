Sejam $x^0 \in \mathbb{R}^n$ e $0\neq d\in \mathbb{R}^n$ tais que $\nabla f(x^0 )^t <0$
$\displaystyle \nabla f(x^0)^t d=\lim_{t\to 0^+}\frac{f(x^0+td)-f(x^0)}{t}<0$
$\displaystyle \frac{f(x^0+td)-f(x^0)}{t}<0$, ou seja $f(x^0+td)<f()x^0,~\forall t\in (0,\epsilon)$

**d** é direção de descida para f a partir de $x^0$

***Teorema*** 
	Seja $f(x)\in \mathbb{R}^n$ de classe $c^1$. Então a direção $-\nabla f(x)$ é a direção de maior descida
	**Demonstração**
	
***Algoritmo***
dado $x^0 \in \mathbb{R}^n$
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $\nabla f(x^0)^td<0$
	Tome t>0 tal que $f(x^k+td)<f(x^k)$
	$x^{k+1}=x^k+td$

As duas _escolhas_ no algoritmo definem os métodos

dado $x^0 \in \mathbb{R}^n$
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $\nabla f(x^0)^td<0$
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)$
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+td$

---
_Obs:_ ele pode parar em um ponto de máximo por azar do passo
_Obs:_ A função pode decair infinitamente na direção escolhida
- Exemplo do uma função que o ponto acaba em um máximo pelo salto e também pode continuar infinitamente pela direita
![[salto_maximo.png|center|400]]

Assim, construímos um *Algoritmo* que permite o passo longe não ser pequeno. Para isso criamos uma constante $\beta$ de proporcionalidade
- Ou podemos escolher a [[Sequência]] abaixo que sempre cairá e atendera aos critérios, mas nunca para e converge para 1, que pode ser nada $$x^k=1+\frac{1}{k}$$
Para evitar estes problemas, colocamos uma nova condição $\|d\|\geq \beta \|\nabla f(x)\|$, que impede que o passo diminuía muito se o [[Gradiente]] ainda é grande

dado $x^0 \in \mathbb{R}^n$ 
dados $\beta >0$
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $\nabla f(x^0)^td<0$ e $\|d\|\geq \beta \| \nabla f(x)\|$ 
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)$
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+td$

---
Aplicamos a [[Regra de Armijo]] ou [[Decréscimo suficiente]] para deixar que ela diminua uma taxa constante

dado $x^0 \in \mathbb{R}^n$ 
dados $\beta >0;~\alpha\in (0, ~1)$ 
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $\nabla f(x^0)^td<0$ e $\|d\|\geq \beta \| \nabla f(x)\|$ 
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)+\alpha t \nabla f(x)^td$  
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+td$

---
dado $x^0 \in \mathbb{R}^n$ 
dados $\beta >0;~\alpha\in (0, ~1),~\gamma \in (0,~1]$  
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $\nabla f(x^0)^td \leq -\gamma \| \nabla f(x^k)\|\|d^k\|$ e $\|d^k\|\geq \beta \| \nabla f(x)\|$ 
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)+\alpha t \nabla f(x)^td$  
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+td$

***Teorema***
	O algoritmo para em algum $\mathbb{R}\in \mathbb{N}$ tal que $\|\nabla f(x^k)\|=0$ ou gera uma [[Sequência]] $(x^k)$ tal que se existe uma subsequência convergente, então ela converge para um [[Ponto estacionário]]
	**Demonstração**
	muita análise
