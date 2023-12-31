SVD - [[Decomposição de valores singulares]]

Seja $A\in \mathbb{R}^{mxn}$ e [[Posto]](A) = r. Então existem números reais $\sigma_1 \geq \sigma_2 \geq ...\geq \sigma_r >0$, uma base [[Ortonomal]] $v_1,v_2,...v_n ~\in \mathbb{R}^n$ , e uma base [[Ortonomal]] $u_1,u_2,...,u_m ~\in \mathbb{R}^m$, tal que $$(*)=\begin{cases} A v_i = \sigma_iu_i \hspace{2cm}A^tu_i = \sigma_iv_i, \hspace{1cm} i=1,2,3,...,r \\Av_i = 0 \hspace{2cm} A^tu_i = 0,\hspace{2cm}  i=r+1, r+2,...,n \end{cases}$$

Observe que $(*)$ implica que $v_1, v_2,...,v_n$ são [[Autovalor]]es de $A^TA$, $u_1,u_2,...u_m$ são autovalores de $AA^t$ e $\sigma^2_1, \sigma^2_2,...,\sigma^2_r$ são todos autovalores não nulos de $AA^t$ e $A^tA$ (Esta observação determina como $(v_i)_n$ devem ser escolhidos)


![[Singular_value_decomposition.gif|center|300]]

Sejam $(v_i)_n$ uma base ortonormal de autovalores de $\mathbb{R}^n$ consistindo de autovalores de $A^TA$, e sejam $(\lambda_i)_n$ seus autovalores associados. Como $A^tA$ é [[Definida semipositiva]], todos os autovalores são não negativos.
Suponhamos que $(v_i)_n$ são ordenados, tal que $\lambda_1 \geq \lambda_2 \geq ... \geq \lambda_n$. Como $r=Posto(A)=Posto(A^tA)$, devemos ter $\lambda_r >0$ e $\lambda_{r+1}=\lambda_n=0$ .
Para i=1,2,3,...,r , definiremos $u_i = \|Av_i\|_2$ e $\displaystyle u_i = \frac{1}{\sigma_i}Av_i$
Assim, temos:
$\|u_i\|_2 = 1$ e $Av_i = \sigma_iu_i, \hspace{0.5cm} i=1,2,...,r$ 

Como $(v_i)_n$ é uma base ortonormal de $\mathbb{R}^n$, então $v_i$ é ortogonal a $v_j$ para $i \neq j$. Sejam $u_i$ e $u_j$ dois vetores com $i \neq j$ 
$\displaystyle\large  <u_i, u_j> = \left \langle \frac{1}{\sigma_i}Av_i, \frac{1}{\sigma_2}Av_j \right \rangle \frac{1}{\sigma_i \sigma_j} \langle Av_i, Av_j\rangle = \frac{1}{\sigma_i \sigma_j} (Av_i)^t(Av_j)=$
$\displaystyle \large \frac{1}{\sigma_i \sigma_j}v_i\underbrace{A^tAv_j}_{\lambda_iv_i} = \frac{1}{\sigma_i \sigma_j}v_i\lambda_iv_j = \frac{\lambda_i}{\sigma_i \sigma_j}v_iv_j = 0$

Portanto $(u_i)_r$ são ortogonais. Dai, e do fato de serem vetores unitários, temos que $(u_i)_r$ são ortonormais

Agora, observe que:
$\large \displaystyle \sigma_i^2 = \|Av_i\|^2 = <Av_i, Av_i> = v_i^tA^tAv_i = v_i^t\lambda_iv_i = \lambda_i \underbrace{v_i^tv_i}_{1} \Rightarrow \sigma_i^2 = \lambda_i$ 

Além disso

Supondo que r<n, então ainda temos que definir $(u_i)_{r+1 \to m}$. 
Temos que $(u_i)_r$ são autovalores de $AA^t$ associados com autovalores não-nulos, como $AA^t \in \mathbb{R}^{mxn}$ e Posto($AA^t$) = r
=> $Nulidade(AA^t)= m-r$

Sejam $(u_i)_{r+1 \to m}$ uma base ortonormal de espaço nulo de $AA^t$. Observe que $(u_i)_{r+1 \to m}$ são autovalores de $AA^t$ com autovalore associado 0(Zero). Temos que $(u_i)_{r+1 \to m}$ são ortogonais a $(u)_r$. Portanto $(u_i)_m$ é uma base ortonormal de $\mathbb{R}^m$ consistindo de autovetores de $AA^t$.
Como Ker($AA^t$) = ker$(A^t)$ temos $A^tu_i =0, \hspace{0.5cm} i=r+1,...,m$

---
Obs:
1) Os números $(v_i)_r$ são chamados de valores singulares de A

Seja k = min{n,m}. Se r<k, é ususal jutar k-r valores singulares zeros $\sigma_{r+1} = ...=\sigma_k =0$. os vetores $v_1, ...,v_n$ são chamados de vetores a direita de A, e $u_1,..,u_m$ são chamados de vetores singulares a esquerda de A. Vetores singulares não são unicamente determinados.

2) $A^t$ tem os mesmos valores singulares de A

Seja $A \in \mathbb{R}^{mxn}$ e Posto(A)=r. Então existe $u \in \mathbb{R}^{mxm}$, $\Sigma \in \mathbb{R}^{nxn}$ tal que u e v são ortogonais, $\Sigma$ tem a forma

$$\Sigma = \begin{bmatrix} \sigma_1 & 0 & 0 & 0 & 0  & ...& 0 \\ 0 & \sigma_2 & 0 & 0 & 0 & ... & 0 \\ 0 & 0 & \sigma_3 & 0 & 0 & ... & 0 \\ .. & ... & ... & ... & ... & ... & ... \\ 0 & 0 & 0 & 0 & \sigma_r & ... & 0 \\  &  & 0 &  &  &  & 0\end{bmatrix}$$
$\sigma_{1}\geq \sigma_{2\geq}...\geq \sigma_{r}>0$ e $A=u\Sigma V^t$
$\displaystyle A=[v_1...v_r|v_{r+1}...v_n]=[u_1...u_r|u_{r+1}...u_m]\Sigma$ 

---
**Exemplo**
Encontre os valores singulares, os vetores singulares a direita e a esquerda da matriz A.
$$A=\begin{bmatrix} 1 & 2 & 0 \\ 2 & 0 & 2\end{bmatrix}_{2_x3}$$
Temos que $A \in \mathbb{R}^{2_x3}$ e $A^{t}\in \mathbb{R}^{3_x2}$  =>
$AA^{t}= \begin{pmatrix}1 & 2 & 0 \\ 2 & 0 & 2\end{pmatrix} \begin{pmatrix}1 & 2 \\ 2 & 0 \\ 0 & 2\end{pmatrix} = \begin{pmatrix}5 & 2 \\ 2 & 8\end{pmatrix}$ => $\begin{pmatrix}5-\lambda & 2 \\ 2 & 8-\lambda\end{pmatrix}$ =>
$det(AA^{t})= (5-\lambda)(8-\lambda) -4=0$ => $\begin{cases}\lambda =4 \\ \lambda =9\end{cases}$ => $\begin{cases}\sigma_{1}= 3 \\ \sigma_{2}= 2 \end{cases}$
Os vetores singulares a esquerda de A são os autovatores de $AA^t$ 
- Resolvendo $(AA^{t}-9I)u=0$ 
=> $\begin{pmatrix}5-9 & 2 \\ 2 & 8-9\end{pmatrix}\begin{pmatrix}a \\ b\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix}$ => $\begin{pmatrix}-4a+2b=0 \\ 2a-b=0\end{pmatrix}$ =>b=2a
$u = \begin{pmatrix}a \\ b\end{pmatrix} = \begin{pmatrix}1 \\ 2\end{pmatrix}$ => $\displaystyle u_{1}= \frac{1}{\|u\|}\begin{pmatrix}1 \\ 2\end{pmatrix}$
- Resolvendo para $\lambda_{2}=4$ 
$\displaystyle u_{2}= \frac{1}{\sqrt{5}}\begin{pmatrix}2 \\ -1\end{pmatrix}$
Logo, $u_{1}= \frac{1}{\sqrt{5}}\begin{pmatrix}1 \\ 2\end{pmatrix}$ e $u_{2}= \frac{1}{\sqrt{5}}\begin{pmatrix}2 \\ -1\end{pmatrix}$ são vetores singulares a esquerda de A. Agora para determinar $v_{1},~v_2,~v_3$ podemos calcular os autovalores de $AA^t$. Mas $v_1$ e $v_2$ podem ser facilmente calculados pela fórmula
$$v_{i}= \frac{1}{\sigma_i}A^tu_i,~~~i=1,2$$
=> $\displaystyle v_{1}= \frac{1}{3\sqrt{5}}\begin{pmatrix}5 \\ 2 \\ 4\end{pmatrix}$, $\displaystyle v_{2}= \frac{1}{2\sqrt{5}}\begin{pmatrix}0 \\ 4 \\ 2\end{pmatrix}$
Para calcular $v_3$, devemos ter $Av_{3}= \theta$ 
$\begin{pmatrix}1 & 2 & 0 \\ 2 & 0 & 2\end{pmatrix}\begin{pmatrix}a \\ b \\ c\end{pmatrix} = \theta$ => $\begin{cases}a=2b \\ a=-c\end{cases}$ => $\begin{pmatrix}-2  \\ 1 \\ 2\end{pmatrix}$ =>$v_{3}= \frac{1}{3}\begin{pmatrix}-2 \\ 1 \\ 2\end{pmatrix}$
A decomposição é 
$$u = \frac{1}{\sqrt{5}}\begin{pmatrix}1 & 2 \\ 2 & -1\end{pmatrix},~~~\Sigma = \begin{pmatrix}3 & 0 & 0 \\ 0 & 2 & 0\end{pmatrix}~~~e~~~v=\begin{pmatrix}\frac{5}{3\sqrt{5}} & 0 & \frac{-2}{3} \\ \frac{2}{3\sqrt{5}} & \frac{2}{\sqrt{5}} & \frac{1}{3} \\ \frac{4}{3\sqrt{5}} & \frac{-1}{\sqrt{5}} & \frac{2}{3}\end{pmatrix}$$

---
[[Análise numérica 1/Quadrados mínimos|Quadrados mínimos]] com SVD
	Sejam $A \in \mathbb{R}^{m_xn}$, r=Posto(A) e $b \in \mathbb{R}^n$. Considere o sistema de equações Ax= b
	com  $x \in \mathbb{R}^n$. Se m>n, então o sistema é sobredeterminado. Logo, Não podemos esperar encontrar uma solução exata. Vamos procurar um x tal que $\|b -Ax\|_2$ seja minimizado.
- Se $m \geq n$ e posto(A)=n, então o problema  de quadrados mínimos tem solução única
- Se $Posto(A) <n$, então a solução é única e existem muitos valores de $x \in \mathbb{R}^n$ para os quais $\|b - Ax\|_2$ é minimizado
