Um dos primeiros a usar integral como área, foi Arquimedes para encontrar $\pi$ 
- ### Lista de primitivas
	$\displaystyle x^a$ --> $\large \displaystyle\frac{x^{a+1}}{a+1}+C$
	
	$\sin(x) \rightarrow -cos(x)+c$ 
	
	$\cos(x) \rightarrow \sin(x)+c$
	
	$\displaystyle \frac{1}{x}$ --> $\ln|x| +C$
	
	$a^x$ --> $\displaystyle \frac{a^x}{\ln a}$
	
	$\displaystyle \frac{1}{1+x^2}$ --> $arctan(x) +C$
	
	$\displaystyle \frac{1}{\sqrt{1\pm x^2}}$ --> $Ln|x+\sqrt{x^2+1}|$

	$Sen^2(x)$ --> $\frac{1}{2}\left( x-\frac{1}{2}Sen(2x)\right)$

***Teorema***
Seja $a<c<b$. Se f é integrável em [a,b], então f é integrável em [a,c] e em [c,b]. Reciprocamente, se f é integrável em [a,c] e em [c,b], então é integrável em [a,b]. Finalmente, se f é integrável em [a,b], então
$$\int_a^bf=\int_a^cf+\int_c^bf$$
	**Demonstração**
	P = {$t_0=a,t_1,...,t_n=b$} $t_j=c$
	P' = {$t_0=a,t_1,...,t_j=c$}
	P'' = {$t_j=c,t_{j+1},...t_n=b$}
	L(f,p) = $\sum_{1}^nm_i(t_i-t_{i-1})=\sum_{1}^jm_i(t_i-t_{i-1})+\sum_{i=j+1}^nm_i(t_i-t_{i-1})$
	Por isso:
	L(f,p) = L(f,P')+L(f,P'')
	U(f,p) = U(f,P')+U(f,P'')
	$[U(f,P')-L(f,P'')]+[U(f,P'')-L(f,P'')]<\epsilon$

***Teorema***
Se f e g são integráveis em [a,b], então f+g é integrável em [a,b] e
$$\int_a^b(f+g)=\int_{a}^bf+\int_a^bg$$
***Teorema***
Se f é integrável em [a,b], então para todo número c, a função cf é integrável em [a,b] e
$$\int_a^bcf=c\int_a^bf$$


---
- **Métodos de primitivas**
	1. Substituição de variável
		$\int f(x)dx$
	2. integral por substituição
		$$\int f(x)g'(x)dx = f(x)g(x)-\int f'(x)g(x)$$
	3. Mudança de variável na integral
		Se f e g' são contínuas, então
		$\displaystyle \int_g(a)^g(b)f(x)dx=\int_a^b(f\circ g(t))g'(t)dt$
		Ex:
		Calcule a área da região limitada pelo gráfico de $f(x)=\sqrt{1-x^2}$, o eixo x entre os pontos x=0 e x=1.
		A=$\int_0^1\sqrt{1-x^2}dx$
		x=g(t)=sen(t)
		$g(a)=sen(a)=0$
		$sen(\pi /2)=1$
		$f(g(t))=\sqrt{1-sen^2(t)}=cos(t)$
		$g'(t)=sen'(t)=cos(t)$
		$\displaystyle \int_0^{\pi /2}cos^2(t)$
	