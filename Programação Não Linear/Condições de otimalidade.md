$f:\mathbb{R}^n\to\mathbb{R}$, tal que $f\in C^1(\mathbb{R}^n)$ 

***Teorema***
Seja $\bar x \in \mathbb{R}^n$ um [[Minimizador]] local de f em $\mathbb{R}^n$. Então, $\nabla f(\bar x)=0$ 
**Demonstração**
	Como $\bar x$ um minimizador local, existe $\epsilon >0$ tal que $f(\bar x)\leq f(x)$ para todo $\|x-\bar x\|<\epsilon$ 

***Teorema***
	Seja $\bar x \in \mathbb{R}^n$ um $\min$ local de f em $\mathbb{R}^n$ então,
	1. $\nabla f(\bar x)=0$
	2. $\nabla^2 f(\bar x)$ [[Definida semipositiva]] 
	**Demonstração**
	Como $\bar x\in \mathbb{R}$ é um [[Minimizador]] local, existe $\epsilon >0$ tal que $f(\bar x)\leq f(x)$ para todo $\|x-\bar x\|< \epsilon$. Dai $\nabla f(\bar x)>0$
	por [[Polinômio de Taylor]] 
	$\displaystyle f(\bar x +td)=f(\bar x)+\underbrace{\nabla f(\bar x)^t(td)}_{0}+\frac{1}{2}(td)^2\nabla f(\xi)(td)$ 
	onde $\xi = \bar x+sd$ com $s \in (0,t)$
	Suponha que $\nabla^2 f(\bar x)$ não é semidefinida positiva, pela [[Matriz Hessiana]] ser [[Contínua]], $d^t\nabla^2 f(\bar x) d<0$  
***Teorema***
	1. $\nabla f(\bar x)=0$
	2. $\nabla^2 f(\bar x)$ é uma [[Matriz definida positiva]]
	**Demonstração**
	Por [[Polinômio de Taylor]]
	$f(x)=f(\bar x)+\nabla f(\bar x)^t(x-\bar x)+\frac{1}{2}(x-\bar x)^t\nabla^2 f(\xi)(x-\bar x)$
	com $\xi = \bar x +t(x-\bar x),~t\in(0,1)$
	como $\nabla^2f(\bar x)$ é definida positiva, existe $\epsilon >0$ tal que para todo $x \in \mathbb{R}^n$ tal que $\|x-\bar x\|< \epsilon$, $\nabla^2f(x)$ é definida positiva
	assim, para $\|x-\bar x\|<\epsilon$, $\nabla^2f(\xi)$ é definida positiva, portanto, se $x\neq \bar x$ 
	$$f(x)=f(\bar x)+\frac{1}{2}\underbrace{(x-\bar x)^t\nabla^2f(\xi)(x-\bar x)}_{0}$$
	$f(\bar x)<f(x)$ para todo $x\neq \bar x$ e $\|x-\bar x\|<\epsilon$
	Logo, $\bar x$ é um minimo local estrito 
	**Exemplo 1**
	$f:\mathbb{R}^2\to \mathbb{R}$, $f(x)=x_1^2+x_2^2$ 
	![[paraboloide.png|center|400]]
	$\nabla f(x)^t=\begin{pmatrix}2x_1 & 2x_2\end{pmatrix}$
	$\nabla^2f(x)=\begin{pmatrix}2 & 0 \\ 0 & 2\end{pmatrix}$
	Pontos estacionários
	$\nabla f(\bar x)=0$ => $\bar x=(0,0)^t$
	$\nabla^2 f(\bar x)=\begin{pmatrix}2 & 0 \\ 0 & 2\end{pmatrix}$ é uma [[Matriz definida positiva]]
	**Exemplo 2**
	![[exemplo2.png|center|400]]
	$f(x)=x_1^3-3x_1+x_2^2$
	$\nabla f(x)=\begin{pmatrix}3x_1^2-3 \\ 2x_2\end{pmatrix}$
	$\nabla^2f(x)=\begin{pmatrix}6x_1 & 0 \\ 0 & 2\end{pmatrix}$
	[[Ponto estacionário]] 
	$\begin{cases}3x_1^2-3=0 \\ 2x_2=0\end{cases}\Rightarrow \bar x_1=\begin{pmatrix}1 \\ 0\end{pmatrix}, \bar x_2 =\begin{pmatrix}-1 \\ 0\end{pmatrix}$
	**Exemplo 3**
	$f(x)=x_1^3+3x_2^2-3x_1x_2^2$
	![[exemplo3.png|center|500]]
	$\nabla f(x)=\begin{pmatrix}3x_1^2-3x_2^2 \\ 6x_2-6x_1x_2\end{pmatrix}$, $\nabla^2f(x)=\begin{pmatrix}6x_1 & -6x_2 \\ -6x_2 & -6-6x_1\end{pmatrix}$
	[[Ponto estacionário]]
	$\begin{cases}3x_1^2-3x_2^2=0 \\ 6x_2-6x_1x_2=0\end{cases}\Rightarrow \bar x_1+\begin{pmatrix}0 \\ 0\end{pmatrix}, \bar x_2=\begin{pmatrix}1 \\ 1\end{pmatrix}, \bar x_3=\begin{pmatrix}1 \\ -1\end{pmatrix}$
	Para o primeiro x
	$\nabla f(\bar x_1)= \begin{pmatrix}0 \\ 0\end{pmatrix}, \nabla^2 f(\bar x)=\begin{pmatrix}0 & 0 \\ 0 & -6\end{pmatrix}$, CN2 mas não CS2
	$\nabla f(\bar x_2)=\begin{pmatrix}0 \\ 0\end{pmatrix}, \nabla^2f(\bar x_2) =\begin{pmatrix}6 & -6 \\ -6 & 0\end{pmatrix}$, CN2, é [[pontos de sela]]
	$\nabla f(\bar x_3)=\begin{pmatrix}0 \\ 0\end{pmatrix}=\begin{pmatrix}6 & 6 \\ 6 & 0\end{pmatrix}$, INDEFINIDA [[pontos de sela]]
	**Exemplo 4**
	$f(x)=x_1^3-x_1x_2....$
	![[exemplo4.png]]	
	
**Condições necessárias de 1º ordem** (CN1): $\bar x$ é minimizador => $\nabla f(\bar x)=0$
**Condições necessárias de 2º ordem** (CN2): $\bar x$ é minimizador => $\begin{cases}\nabla f(\bar x)=0\\ \nabla^2 f(\bar x)~~\text{é semidefinida positiva}\end{cases}$ 
**Condições suficientes de 2º ordem**:
$\begin{cases}\nabla f(\bar x)=0\\ \nabla^2f(\bar x)~~ \text{é definida positiva}\end{cases}$ => $\bar x$ é minimizador

***Exemplo 1***
$f:\mathbb{R}^2\to \mathbb{R}$, $f(x)=x_1^4+x_1x_2^2-2x_1x_2-3x_1+1$
$\nabla f(x)=\begin{pmatrix}4x_1^3 +x_2^2-2x_2-3 \\ 2x_1x_2-2x_1\end{pmatrix}$ e $\nabla^2 f(x)=\begin{pmatrix}12x_1^2 & 2x_2-2 \\ 2x_2-2 & 2x_1\end{pmatrix}$ 
Do gradiente, encontramos os candidatos
$\bar x_1=\begin{pmatrix}0  \\ 3\end{pmatrix},~\bar x_2=\begin{pmatrix}0 \\ 1\end{pmatrix},~\bar x_3=\begin{pmatrix}1 \\ 1\end{pmatrix}$
Para o _primeiro_
$\nabla^2 f(\bar x_1)=\begin{pmatrix}0 & 4 \\ 4 & 0\end{pmatrix}$ é uma [[Matriz]] indefinida por ter [[Autovalor]] negativo e positivo
Para o _segundo_
$\nabla^2 f(\bar x_2)=\begin{pmatrix}0 & -4 \\ -4 & 0\end{pmatrix}$ Novamente é uma [[Matriz]] indefinida
Para o _Terceiro_
$\nabla^2 f(\bar x_3)=\begin{pmatrix}12 & 0 \\ 0 & 2\end{pmatrix}$ Definida positiva, então é um [[Mínimo]] 

***Exemplo 2***
$f:\mathbb{R}^2\to \mathbb{R}$ $f(x)=x_1^2-2x_1\cos(x_2)+1$ 
$\nabla f(x)= \begin{pmatrix}2x_1-2cos(x_2) \\ 2x_1\sin(x_2)\end{pmatrix}$ e $\nabla^2 f(x) =\begin{pmatrix}2 & 2\sin(x_2) \\ 2\sin(x_2) & 2x_1\cos(x_2)\end{pmatrix}$
Encontramos os candidatos que satisfaçam $\nabla f(x)=0$
$\bar x_1=\begin{pmatrix}0 \\ \frac{\pi}{2}+n\pi\end{pmatrix}$ e $\bar x_2=\begin{pmatrix}(-1)^n  \\ n\pi \end{pmatrix}$ 
Agora avaliando os candidatos na [[Matriz Hessiana]]
$\nabla^2f(\bar x_1) = \begin{pmatrix}2 & 2\sin(\pi /2+n\pi) \\ 2\sin(\pi /2+n\pi) & 0\end{pmatrix}$ 
