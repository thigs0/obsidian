O método é o [[Métodos de direções de descida]] porém, tomamos
$$\boxed{d^k=-\nabla f(x^k)}$$
Substituindo no código do método de direção de descida
dado $x^0 \in \mathbb{R}^n$ 
dados $\beta >0;~\alpha\in (0, ~1),~\gamma \in (0,~1]$  
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome $d=\nabla f(x^k)$ tal que $-\nabla f(x^k)^t\nabla f(x^k) \leq -\gamma \| \nabla f(x^k)\|\|-\nabla f(x^k)\|$ e $\|-\nabla f(x^k)\|\geq \beta \| \nabla f(x^k)\|$ 
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)+\alpha t \nabla f(x^k)^t\nabla f(x^k)$  
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+t\nabla f(x^k)$

Observamos que qualquer valor de $\gamma$ é valido. Qualquer valor $\beta >1$ também é válido. Então simplificamos o algoritmo

dado $x^0 \in \mathbb{R}^n$ 
dados $\beta >1;~\alpha\in (0, ~1)$  
**Enquanto** $\|\nabla f(x^0)\|\neq 0$ 
	Tome d tal que $-\nabla f(x^k)^t\nabla f(x^k) \leq -\gamma \| \nabla f(x^k)\|\|-\nabla f(x^k)\|$ e $\|-\nabla f(x^k)\|\geq \beta \| \nabla f(x^k)\|$ 
	Tome t=1
	**Enquanto** $f(x^k+td)\geq f(x^k)+\alpha t \nabla f(x^k)^t\nabla f(x^k)$  
		faça t<- t/2; ou [[Backtracking]]
	$x^{k+1}=x^k+t\nabla f(x^k)$


