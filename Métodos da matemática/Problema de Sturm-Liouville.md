Essa classe de problemas aparecem na resolução de [[Equações separáveis]] para [[EDP]]s 

**Exemplo**
$$y'' +\pi^2y=0,~~0<x<1,~~y(0)=y(1)=0$$
A solução dessa equação é $$y(x)=c_1\sin(\pi)+c_2\cos(\pi x)$$
para o problema $y(x)=c_1sin(\pi x)$ 


Para a forma ampla deste exemplo, temos
$$y''+\lambda y=0,~~~0<x<1,~~y(0)=y(1)=0$$
1) No primeiro caso $\lambda >0$
		Seja $\lambda = k^2 >0$
		Neste caso a solução é $y(x)c_1\sin (kx)+c_2\cos(kx)$
		Com as condições $\begin{cases} y(0) \Rightarrow c_2=0\\ x=1,~y(1)=c_1\sin(k) \end{cases}$
		Para que $y(1)=0$ seja verdade $c_1=0$ ou $\sin(k)=0$
		Retiramos a primeira por ser trivial
		Por fim $\lambda_n = n^2\pi^2$
2) No Segundo caso $\lambda=0$
		A solução é $y(x)=ax+b$
		$y(0)=y(1)=0\Rightarrow a=b=0$
		Temos somente a solução trivial
3) No terceiro caso $\lambda>0$
		Seja $\lambda = -k^2,~k>0$
		A solução é $y(x)=c_1\sinh(kx)+c_2\cosh(kx)$
		Temos $y(0)=0\Rightarrow c_2=0$
		com isso $x=1, ~~y(1)=c_1\sinh(k)$
		Para $y(1)=0$ temos duas possibilidades $\begin{cases} c_1=0\\ \sin(k)=0 \end{cases}$
		Como $k>0$ temos que $c_1=0$ que é a solução trivial


### Formulação do problema
Sendo $L[y]=\frac{d}{dx}\left( p(x)\frac{dy}{dx} \right)-q(x)y$
Um [[PSL]] é um problema da forma
$$\begin{cases}L[y]=-\lambda \rho(x)y,~~~ a<x<b\\ \text{Condição de contorno}\end{cases}$$
Um [[PSL regular]] é um caso especial
$$\begin{cases}L[y]=-\lambda \rho(x)y,~~~ a<x<b\\ \\ \alpha_1y(a)+\alpha_2y'(a)=0\\ \beta_1y(b)+\beta_2y'(b)=0\end{cases}$$
Onde $\alpha_1,\alpha_2,\beta_{1},\beta_2$ são constantes tais que $$\begin{cases} \alpha_1^2+\alpha_2^2>0\\ \beta_1^2+\beta_2^2>0\\ p(x),p'(x),q(x)\rho(x)~~\text{São contínuas em [a,b]}\\p(x)>0,~\rho(x)>0,~\forall x\in [a,b] \end{cases}$$
Um [[PSL Singular]] é aquele onda $p(x)>0$ e/ou $\rho(x)>0$
Não valem em um dos extremos 

[[Autofunção]] é a nomenclatura de um [[PSL]] com solução não trivial, o valor de $\lambda$ associado é um [[Autovalor]] e os [[Conjuntos]]  de autovalores é o [[Espectro do PSL]]

**Exemplo**


### [[PSL regular]]
Se o PSL está na forma adjunta, vale a [[Identidade de Lagrange]]
ou seja
$$v(x)L[u(x)]-u(x)L[v(x)]=\frac{d}{dx}Q[u,v](x)$$
-> $$Q[u,v](x)=p(x)[v(x)u'(x)-u(x)v'(x)]$$
Integrando a identidade acima de a até b, obtemos
$$\int_a^b (v(x)L[u(x)]-u(x)L[v(x)])dx=p(x)[v(x)u'(x)-u(x)v'(x)]|_a^b$$
Agora considerando que o PSL regular é satisfeito. Obtemos
$$\int_a^b (v(x)L[u(x)]-u(x)L[v(x)])dx=0$$

**Teorema** em um PSL regular
1) Os [[Autovalor]]es $\lambda$ são reais
2) As autofunções correspondentes a autovalores distintos são ortogonais com peso $\rho(x))$
3) a cada autovalor correspondente apenas uma autofunção real independente em outras palavras, os autovalores são simples