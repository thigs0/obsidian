Essa classe de problemas aparecem na resolução de [[Equações separáveis]] para [[EDP]]s 
Mônica de castro henriques

$$\begin{cases}\mathbb{L}[u]=\lambda \rho(x)u(x)\\ +\text{Condições de contorno}\end{cases}$$


$<v,\mathbb{L}[u]>=\int_0^1 v(-u'')dx=-\int_0^1(vu')'-v'u'dx$
$-vu'|_0^1 +\int_0^1 (v'u)'dx-\int_0^1 v''udx=(v'u-vu')|_0^1+\int_0^1 (-v'')udx$


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
**Demonstração:**
$\mathbb{L}[y]=\lambda\rho y$; $\mathbb{L}[y^*]=\lambda^*\rho y^*$ 
com $0=<y^*,\mathbb{L}[y]>-<\mathbb{L}[y^*],y=<y^*,\lambda \rho y>-<\lambda^*\rho y^*,y>=(\lambda-\lambda^*)<y^*,\rho y>$
2) As autofunções correspondentes a autovalores distintos são ortogonais com peso $\rho(x))$
**Demonstração:**
$\mathbb{L}[u]=\lambda \rho u$
$\mathbb{L}[v]=\mu \rho v$
como $0=<u,\mathbb{L}[v]>-<\mathbb{L}[u],v>=<u,\mu\rho v>-<\lambda \rho u,v>$
$=\mu<u,\rho v>-\lambda<\rho u,v>=(\mu-\lambda)\int_a^b uv\rho dx=0$ => $<u,v>_\rho =0$ 
3) a cada autovalor correspondente apenas uma autofunção real independente em outras palavras, os autovalores são simples
4) O PSL regular possui uma [[Cálculo 3/Sequência|Sequência]] infinita de [[Autovetor]]es reais $\lambda_0<\lambda_1<\lambda_2<...$ com $\lim_{n\to \infty} \lambda_n=\infty$. As autofunções $y_n$ corresponde a $\lambda_n$ possui exatamente n zeros no intervalo (a,b)

##### Exemplo
$\begin{cases}y''+2y'+y=-\lambda y\\ y(0)=0,~y'(1)=0\end{cases}$
- tomemos $\lambda=-k^2,~, k\neq 0\rightarrow \lambda <0$
$y''+2y'+y=k^2y\Rightarrow y''+2y'+(1-k^2)y=0$ 
usando a solução com a  [[Fórmula de Euler]]
$y=e^{ax}$ -> $a^2e^{ax}+2ae^{ax}+e^{ax}=e^{ax}(a^2+2a+1)=0$ por [[Solução da equação de segundo grau]]
$a=-1$ 
mas ao analisarmos as condições de contorno $y(0)=e^{-x}=1\neq 0$ então não temos solução nesse caso
- tomemos $\lambda=0$ 
então a equação fica $y''+2y'+y=0$, novamente usando as condições acima a solução é 
$y(x)=e^{ax}$ com $x=-1$ e a solução não existe pela analise das condições de contorno
- Tomemos $\lambda=k^2,k\neq 0$
$y''+2y'+y=-k^2y\Rightarrow y''+2y'+(1+k^2)y=0$ e usando novamente os mesmos métodos
$y=e^{ax}$ => $y(x)=e^{-x}(e^{kx}+e^{-kx})$. Agora analisando as condições de contorno
$y(0)=0$ => 

##### dw
Considere $a+\epsilon\leq x\leq b,\epsilon>0$
$\int_{a+\epsilon}^b (u\mathbb{L}(v)-v\mathbb{L}(u))dx=-\rho(a+\epsilon)[u'(a+\epsilon)v(a+\epsilon)-u(a+\epsilon)v'(a+\epsilon)]+\text{o que acontece em x=b}=0$
Tomando $\epsilon\to 0$ e uma vez que $\rho(a)=0$, vemos que se u e v satisfazem
$$\lim_{x\to a}|y(x)|<\infty$$
então
$\lim_{\epsilon\to 0}\rho(a+\epsilon)[v'(a+\epsilon)v(a+\epsilon)-v(a+\epsilon)u'(a+\epsilon)]=0$
**Exemplo**
$\begin{cases}-\frac{d}{dx}(x\frac{dy}{dx})+\frac{v^2}{x}y=K^2xy~~0<x<a\\ y(a)=0;~\lim_{x\to a}|y(x)|<\infty \end{cases}$
a solução são as [[Funções de Bessel]]
$y(x)=AJ_v(kx)+BY_v(kx)$ com $y(a)=J_v(ka)=0\Rightarrow Ka=\alpha_{vn},~~n=1,2,3,...~~~~K_{vn}=\frac{\alpha_{vn}}{a},~~n=1,2,3,...$ 
sabemos que $\displaystyle \int_0^aJ_v\left( \frac{\alpha_{vn}}{a}x \right)J_v\left( \frac{\alpha_{vn}}{a}x \right)xdx=0,~~se~n\neq m$
então $f(x)=\sum\limits_{n=1}^\infty c_nJ_{vn}(\frac{\alpha_{vn}}{a}x)$
com $\displaystyle c_n=\frac{<f(x),J_v(\frac{\alpha_{vn}}{a}x)>}{<J_v(\frac{\alpha_{vn}}{a}x),J_v(\frac{\alpha_{vn}}{a}x)>}=\frac{\int_{0}^a f(x)J_v(\frac{\alpha_{vn}}{a}x)xdx}{\int_{0}^a J_v^2(\frac{\alpha_{vn}}{a}x)xdx}$ 
**Exemplo**
Considere $-\frac{d}{dx}\left( (1-x^2)\frac{dy}{dx} \right)=n(n+1)y,~~-1<x<1$ [[Equação de Legendre]]
$y(x)=AP_n(x)+\underbrace{BQ_n(x)}_{descartamos}$
$y(x)=(1-x^2)(u'v-uv')|_{-1}^1$
o problema é singular nos dois extremos

**Exemplo**: Problema do poço infinito
Resolva $\begin{cases}y''=-\lambda y,~~-L<x<L\\ y(-L)=y(L)=0\end{cases}$
1) O problema é singular ou regular?
Para isso verificamos que as condições são homogêneas $\begin{cases}y(L)=0\\ y(-L)=0\end{cases}$
temos também que $y''=-\lambda y\Rightarrow (1.y')'=-\lambda 1.y\Rightarrow \begin{cases}p(x)=1\\ \rho(x)=0\end{cases}$
logo este é um PSL regular
2) Encontre o espectro ($\lambda ~~- y_\lambda$)
Separamos em casos
- $\boxed{\lambda=-w^2<0}$ 
$y''=w^2y\Rightarrow y_w(x)=A_w\cosh(wx)+B_w\sinh(wx)$, usaremos as condições de contorno
- $y(L)=0\Rightarrow$  
- $\boxed{\lambda =0}$
$y''=0\Rightarrow y_0(x)=A_0+B_0x$ usaremos as condições de contorno
- $y(L)=0\Rightarrow A_0+LB=0$ e $y(-L)=0\Rightarrow A_0-LB=0$ => $A_0=0$ e $B_0=0$
- E a solução trivial não é uma solução válida
- $\boxed{\lambda=w^2>0}$
$y''= -w^2y\Rightarrow y_w(x)=A_w\cos(wx)+B_w\sin(wx)$ usaremos as condições de contorno
- $y(L)=0$, $A_w~e~B_w$ não podem ser nulos ao mesmo tempo (solução trivial)
- Se $B_w=0\Rightarrow \cos(wL)=0\Rightarrow w=\frac{(2n+1)\pi}{2L},~~n\in N$
	- Nesse caso $\displaystyle \lambda =w^2=\frac{(2n+1)^2\pi^2}{4L^2}~~-~~\cos\left( \frac{2n+1}{2L}\pi x \right),~~n=0,1,2,3,...$
- Se $A_w=0\Rightarrow \sin(wl)=0\Rightarrow w=\frac{n\pi }{L}$
	- Nesse caso $\displaystyle \lambda=w^2=\frac{n^2\pi^2}{L^2}~~-~~\sin\left( \frac{n\pi x}{L} \right),~~n=1,2,3,...$
$f(x)=x^2-L^2=0$ $\sum\limits_{n=1}^\infty b_n y_n^s(x)+\sum\limits_{n=0}^\infty a_ny_n^c(x)\leq y_m^s,f(x)> = <y_m^s, \sum\limits_{\lambda_m}b_my_m^s(x)+\sum\limits_{\lambda_m^c}a_ny_n^c(x)>=b_n||y_m^s||^2$ 
$b_m=\frac{<y_m^s,f(x)>}{||y_m^s||^2}$
$$b_n=\frac{1}{L}\int_{-1}^1f(x).\sin\left( \frac{n\pi x}{L} \right)dx$$
$$a_n=\frac{1}{L}\int_{-1}^1f(x)\cos\left(\frac{(2n+1)}{2L}\pi x\right)dx$$
$$f(x)=\sum\limits_{n=0}^\infty \left( a_n\cos\left( \frac{(2n+1)}{2L}\pi x \right)+b_n\sin\left( \frac{n\pi x}{L} \right) \right)$$

