Queremos $$\begin{align}\min f(x)\\ s.a :Ax=b\end{align}$$
$\displaystyle f:\mathbb{R}^{n}\to\mathbb{R},f\in c^2, A\in \mathbb{R}^{m\times n}, b\in \mathbb{R}^{m} s=\{x\in \mathbb{R}^n|Ax=b\}\neq \emptyset$ 

 **Exemplo de problema**
 $$\boxed{\begin{align}\min x_1^2+2x_2^2\\ s.a:x_1+x_2=3\end{align}}$$
 temos que a restrição forma uma reta e a função a ser minimizada tem sua curvas de níveis, de modo que queremos a menor curva que toque a reta e assim irá tangenciar ela
 ![[Exemplo_irrestrito.png|500]]
 Vemos que o [[Gradiente]] da função deve ser um múltiplo do gradiente da reta
 $\nabla f(x_1,x_2)=\begin{bmatrix}2x_1\\ 4x_2\end{bmatrix}= A^t\lambda=\begin{bmatrix}1\\1\end{bmatrix}\lambda \Rightarrow \begin{cases}2x_1 =\lambda \\ 2x_2=\lambda\end{cases}\Rightarrow x_1=2x_2$
Temos uma nova reta, e a solução deve estar neste nova reta e na anterior
$$\begin{align}x_1-2x_2=0\\ x_1+x_2=3\end{align} \Rightarrow x=\begin{pmatrix}2\\1\end{pmatrix}$$

Com esta ideia em mente, expandiremos.

$Im(A) = \{Ax\in \mathbb{R}^m |x\in \mathbb{R}^n\} \subset \mathbb{R}^m$
$Im(A^{t})= \{ A^ty\in \mathbb{R}^n |y\in \mathbb{R}^m\} \subset \mathbb{R}^n$
$\mathscr{N}(A) =\{ x\in \mathbb{R}^n | Ax=0\} \subset \mathbb{R}^n$   

Seja $\bar x\in S$ 

#### Teorema
Seja $x$ um elemento do conjunto de restrição, então ele pode ser representado pelo [[Minimizador]] do nosso problema  e um vetor no [[Núcleo]] de A
$$x \in S \Leftrightarrow x=\bar x +u, u\in \mathscr{N}(A)$$
$$\min f(\bar x +z\gamma)=g(\gamma), ~s.a~ \gamma \in \mathbb{R}^k$$
temos 
$\nabla g(\gamma)=z^t\nabla f(\bar x +z\gamma)$ 
$\nabla^2 g(\gamma) =z^t\nabla^2 f(\bar x + z\gamma)z$

**Condição necessária de 1° ordem**
$\nabla g(\gamma^*)=0 \Rightarrow Z^t\nabla f(\bar x +Z\gamma^*)=0\Rightarrow Z^t\nabla f(x^*)=0$
$z_i^t \nabla f(x^k)=0,i=1,2,...,k$] -> $\nabla f(x^k)\perp \mathscr{A}$ 

-> $\nabla f(x^*)=A^t\lambda^*, \lambda \in \mathbb{R}^m$ 

**Condição necessária de 2° ordem**
Seja $x^*\in \mathbb{R}^n$ um [[Minimizador]] local de f sujeito a $Ax=b$ tal que
1. $\nabla f(\bar x)=A^t\lambda^*$
2. $y^t\nabla^2 f(\bar x)y\geq 0, \forall y\in \mathscr{N}(A)$


**Exemplo**
$$\begin{align}\min x_3x_2^2-x_1^2\\ s.a:\begin{cases}x_1+x_2+x_3\\ x_1-x_2-x_3\end{cases}\end{align}$$
temos $f(x)=x_3x_2^2-x_1^2$
$\nabla f(x)=\begin{pmatrix}-2x_1 \\ 2x_2x_3 \\ x_2^2\end{pmatrix}$
$\nabla^2 f(x)=\begin{pmatrix}-2 & 0 & 0 \\ 0 & 2x_3 & 2x_3 \\ 0 & 2x_2 & 0\end{pmatrix}$

**CN1**
$\nabla f(x) = A^t\lambda$
$\begin{pmatrix}-2x_1 \\ 2x_2x_3 \\ x_2^2\end{pmatrix}=\begin{pmatrix}1 & 1 \\ 1 & -1 \\ 1 & -1\end{pmatrix}\lambda=\begin{pmatrix}1 \\ 1 \\ 1\end{pmatrix}\lambda_1+\begin{pmatrix}1 \\ -1 \\ -1\end{pmatrix}\lambda_2$
temos 
$\begin{cases}-2x_1=\lambda_1+\lambda_2\\ 2x_2x_3=\lambda_1-\lambda_2\\ x_2^2=\lambda_1-\lambda_2 \\ x_1+x_2+x_3=7\\ x_1-x_2-x_3=1\end{cases}$


$d \in \mathbb{R}^n$, $x \in S$ -> $x+td \in S$ e $\nabla f(x)^td<0$ 

$\begin{align}A(x+td)=b \\ Ax+tAd=b\\ tAd=0\\ Ad=0\\ d\in \mathscr{N}(A)\end{align}$

$\bar x \in S$, $g(\gamma)=f(\underbrace{\bar x +Z\gamma}_{x})$ 
$Z\in \mathbb{R}^{n\times k}$ , k = n - [[Posto]](A), $\gamma \in \mathbb{R}^k$
$d=Zw, w\in \mathbb{R}^k$
$\nabla f(x)^td=\nabla f(x)^tZw = [Z^t\nabla f(x)]^tw = \nabla g(\gamma)^tw$

e temos $$\begin{align}g(\gamma) = f(\bar x + Z\gamma)\\ \nabla g(\gamma)= Z^t\nabla f(\bar x+Z\gamma)\\ \nabla^2g(\gamma)=Z^t\nabla^2f(\bar x+Z\gamma)Z\end{align}$$
##### Método 1
$\begin{cases}d=Zw\\ w=-\nabla g(\gamma)=-Z^t\nabla f(x)\end{cases}$

$d = -ZZ^t\nabla f(x)$

##### Método 2
$\begin{cases}d=Zw\\ \nabla^2 g(\gamma)w=-\nabla g(\gamma)\Rightarrow Z^t\nabla^2 f(x)Z-Z^t\nabla f(x)\end{cases}$
$d=-Z(Z^t\nabla^2 f(x)Z)^{-1}Z^t\nabla f(x)$

$-\nabla f(x)=\underbrace{d}_{\in \mathscr{N}(A)} ~\oplus~ \underbrace{v}_{\in Im(A^t)}= Zw+A^ty$, multiplicamos por $Z^t$
-> $-Z^t\nabla f(x)=Z^tZw+Z^tA^ty=Z^tZw+\underbrace{(AZ)^ty}_{0} \Rightarrow w =-(Z^tZ)^{-1}Z^t\nabla f(x)$


[[Posto]](A) = m
$\begin{align}-\nabla f(x)=d+v\\ -\nabla f(x)=d+A^ty\\ -A\nabla f(x)=\underbrace{Ad}_0 + AA^ty\\ y=-(AA^t)^{-1}A\nabla f(x)\end{align}$

$d = -\nabla f(x)+A^t(AA^t)^{-1}A\nabla f(x)$
$d=-[I-A^t(AA^t)^{-1}A]\nabla f(x)$
