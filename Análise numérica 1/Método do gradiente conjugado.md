- Queremos minimizar a função quadrática $f(x)=\frac{1}{2}x^tAx-b^tx+c$
- E sabemos que $\nabla f(x)=Ax-b$
- Se a matriz é mal condicionada, esse método é altamente suscetível aos erros de arredondamento

O [[Análise numérica 1/Método do gradiente]] usava a aproximação $x_{k+1}=x_k+\alpha_k d_k$. O que limita o movimento de aproximação em uma dimensão. Assim, a ideia do método do gradiente conjugado é adicional mais variáveis afim de permitir um movimento mais rápido de aproximação.

**Exemplo de ideia**
Dizemos que o próximo passo será $\displaystyle x_{k+1}=x_k+\alpha_k d_k + \beta_k e_k$ 
obtemos que para minimizar a função, veremos a [[Derivada Parcial]] 
$$\begin{cases}\displaystyle \frac{\partial f(x+\alpha d+\beta e)}{\partial \alpha} = d^t(Ax+\alpha Ad+\beta Ae-b)=0\\ \displaystyle\frac{\partial f(x+\alpha d+\beta e)}{\partial \beta}=e^t(Ax+\alpha Ad+\beta A e -b)=0\end{cases}$$
Esses casos podem ser representados em uma [[Matriz]] como um [[Sistema linear]]
$$\large \begin{bmatrix}d^tAd & d^tAe \\ e^tAd & e^tAe\end{bmatrix}\begin{pmatrix}\alpha \\ \beta \end{pmatrix}=\begin{bmatrix} d^t(b-Ax) \\ e^t(b-Ax) \end{bmatrix}$$
Assim, caímos na resolução de um sistema para resolver o sistema que queríamos.
De tal modo que ao ao adicionarmos n variáveis a mais, precisamos resolver um sistema de ordem n.

Para facilitar a resolução da matriz, forçamos termos 0s na diagonal secundária para formar uma matriz esparsa. Normalmente escolhemos um vetor de $e~ou~d$ e construímos o outro de modo que $e^tAd=0$

Para isso, construímos uma nova definição
**Definição**
Dados $(v_i)$ vetores, quero $(w_i)$ conjugados a ele por construção com o [[Processo de Gram-Schmidt]]
$w_1=v_1$
$w_2=v_2-\gamma_{21}w_1$ 
$\displaystyle \gamma_{ij}=\frac{v_i^tAw_j}{w_{j}^tAw_j}$

**Teorema**

---
**Pseudo-código**
Dado $x_0$
**Para** k=0,1,2,3,..
	$r_k=b-Ax_k$
	$\displaystyle d_k=r_k-\gamma_{k_1}d_1-\gamma_{k_2}d_2-...\gamma_{k_{k-1}}d_{k-1}$
	$\displaystyle \alpha_k = \frac{d_k^tr_k}{d_k^tAd_k}$ 
	$x_{k+1}= x_k+\alpha_kd_k$

-------

**Teorema**
Considere o problema $\displaystyle \min f(x)=\frac{1}{2}x^TAx-b^Tx+c$, onde $A \in \mathbb{R}^{n_xn}$ é uma [[Matriz definida positiva]], $b \in \mathbb{R}^n$ e $c \in \mathbb{R}$. (Equivalente à resolução do [[Sistema linear]] Ax=b). Sejam $d_0,d_1,...,d_{n-1}$ direções A-conjugados e seja $x^{(0)}\in \mathbb{R}^n$ em ponto inicial arbitrário. Definimos
$$x^{(k+1)}=x^{(k)}+s_kd_k, \hspace{2cm}k=0,1,2,3,...$$
Então
i. $\displaystyle s_k=\frac{-\nabla f(x^{(k)})^{td_k}}{d_k^tAd_k}$
ii. $\nabla f(x^{(k)})^{td_j=0,}\hspace{2cm} j=0,1,2,3,...$
iii. $x^{(n)}$ é o mínimo de f em $\mathbb{R}^n$

Dem:
	i. 

----
**Exemplo**
Considere a matriz definida positiva
$$A=\begin{bmatrix}4 & 3 & 0 \\ 3 & 4 & -1 \\ 0 & -1 & 4\end{bmatrix}, \hspace{2cm}b=\begin{pmatrix}24 \\ 30 \\ -24\end{pmatrix}$$
Seja $d_0=\begin{pmatrix}1 \\ 0 \\ 0\end{pmatrix}$ , $d_1=\begin{pmatrix}-3/4 \\ 0 \\ 0\end{pmatrix}$ e $d_2=\begin{pmatrix}-3/7 \\ 4/7 \\ 1\end{pmatrix}$
Temos que:
	$d_0^tAd_1=\begin{pmatrix}1 & 0 & 0\end{pmatrix}\begin{pmatrix}4 & 3 & 0 \\ 3 & 4 & -1 \\ 0 & -1 & 4\end{pmatrix}\begin{pmatrix}-3/4 \\ 1 \\ 0\end{pmatrix}=\begin{pmatrix}1 & 0 & 0\end{pmatrix}\begin{pmatrix}0 \\ 7/4 \\ -1\end{pmatrix}=0$ 
	$d_0^tAd_2=\begin{pmatrix}1 & 0 & 0\end{pmatrix}\begin{pmatrix}4 & 3 & 0 \\ 3 & 4 & -1 \\ 0 & -1 & 4\end{pmatrix}\begin{pmatrix}-3/7 \\ 4/7 \\ 1\end{pmatrix}=\begin{pmatrix}1 & 0 & 0\end{pmatrix}\begin{pmatrix}0 \\ 1 \\ 24/7\end{pmatrix}=0$
	$d_1^tAd_2=\begin{pmatrix}-3/4 & 1 & 0\end{pmatrix}\begin{pmatrix}4 & 3 & 0 \\ 3 & 4 & -1 \\ 0 & -1 & 4\end{pmatrix}\begin{pmatrix}-3/7 \\ 4/7 \\ 1\end{pmatrix}=0$
	Portanto $\{d_0, d_1,d_2\}$ é A-conjugados
	Agora resolvemos o sistema com o método com o vetor nulo como inicio.
	$x^{(k+1)}=x^{(k)}+s_kd_k$
