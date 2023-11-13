$\begin{align}\textbf{Problema primal}\\ \min f(x)=c^tx\\ s.a:\begin{cases}Ax\geq b\\ x\geq 0\end{cases}\end{align}$                     $\begin{align}\textbf{Problema Dual}\\ \max g(p)=b^tp\\ s.a:\begin{cases}A^tp\leq c\\ p\geq 0\end{cases}\end{align}$
- Existe uma dependência entre condições do primal e do dual
- Na solução ótima não é possível $x_j >0$ e $(A^tp)_j<c_j$
	Assim como não é possível $p_i>0$ e $(Ax)_i>b_i$


Assim *Folgas complementares* é:
$$\begin{align}p^t(Ax-b)=0\\ x^t(c-A^tp)=0\end{align}$$
ou $$\begin{cases}se~x_j>0 \Rightarrow z_j=0\\ se~z_j>0 \Rightarrow x_j=0\end{cases}$$

#### Teorema (Folgas complementares)
Sejam $x$ e $p$ soluções factíveis dos problemas primal e dual, respectivamente. Os vetores $x$ e $p$ são soluções ótimas dos respectivos problemas se,e somente se
1. $p_i(a_i^tx-b_i)=0,~i=1,2,...,m$
2. $(c_j-p^tA_j)x_j=0,~j=1,2,...,n$

**Demonstração**:
sejam $u_{i}= p_i(a_i^tx-b_i)$ e $v_j=(c_j-p^tA_j)x_j$ 

$\begin{align}u+v\\ \sum_{i=1}^m p_i(a_i^tx-b_i)+\sum_{j=1}^n (c_j-p^tA_j)x_j\\ \sum_{i=1}^mp_ia_i^tx-\sum\limits_{i=1}^nc_jx_j-\sum\limits_{j=1}^n p^tA_jx_j~(\text{Distribuímos os valores})\\ p^tAx-\sum\limits_{i=1}^mp_ib_i + \sum\limits_{j=1}^n c_jx_j-p^tAx~\text{(Simplificamos a notação)}\\ c^tx-b^tp \end{align}$ 
pelo [[Teorema forte da dualidade]], temos que 
$$c^tx=b^tp\Rightarrow \sum u_i + \sum v_j=0 \Rightarrow u_i=v_j=0$$
Por estarmos em uma solução ótima, o menor valor é 0.

Caso tenhamos que $u=v=0$, pelo corolário 2 do [[Teorema fraco da dualidade]], obtemos que é uma solução ótima


#### Exemplo
$\begin{align} \min v=13x_1+10x_2+6x_3\\ s.a: \begin{cases} 5x_1+x_2+3x_3=8\\ 3x_1+x_2=3\\ x_1\geq 0,x_2\geq 0, x_3\geq 0\end{cases}\end{align}$   $\begin{align}\max w=8p_1+3p_2\\ s.a:\begin{cases}5p_1+3p_2\geq 13\\ p_1+p_2 \leq 10 \\ 3p_1\leq 6\end{cases}\end{align}$

com solução ótima em $p^*=\begin{pmatrix}2 \\ 1\end{pmatrix}$, $w^*=19$ 

$$\begin{align}p_1(5x_1+x_2+3x_3-8=0) \hspace{2cm}\Rightarrow 5x_1+x_2+3x_3=8\\ p_2(3x_1+x_2-3)=0\hspace{2cm}\Rightarrow 3x_1+x_2=3\\ x_1(13-5p_1-3p_2)=0\hspace{2cm}\Rightarrow x_1\geq 0\\ x_3(6-3p_1)=0 \hspace{2cm}\Rightarrow x_3\geq 0\end{align}$$
então obtemos $x=\begin{pmatrix}1 & 0 & 1\end{pmatrix}^t$


<mark style="background: #FFF3A3A6;">Para</mark> 
$\begin{align} \min z=2x_2+x_2+4x_3\\ s.a:\begin{cases}-2x_1+x_2+x_3\geq 1\\ x_1-2x_2+x_3\geq -1\\ x_1\geq 0, x_2\geq 0, x_3\geq 0\end{cases}\end{align}$   

o dual é 
$\begin{align}\max p_1-p_2 \\ s.a:\begin{cases}-2p_1+p_2\leq 2\\ p_1-2p_2\leq 1\\ p_1-p_2\leq 4\\ \text{p livre}\end{cases}\end{align}$

```functionplot
---
title: Região
disableZoom: false
bounds: [-4,9,-4,9]
grid: true
xLabel: x
yLabel: y
---

f(x) = (2+2*x)
g(x) = (-1+x)/2
h(x) = (-4+x)

```

Graficamente temos a [[Resolução gráfica]] sendo $p = \begin{pmatrix}7 & 3\end{pmatrix}$ 
Assim, 
$$\begin{align}p_1(-2x_1+x_2+x_3-1)=0  \Rightarrow 7(-2x_1+x_2+x_3-1)=0\\ p_2(x_1-2x_2+x_3+1)=0\Rightarrow 3(x_1-2x_2+x_3+1)=0\\ x_1(2+2p_1 -p_2)=0 \Rightarrow x_1(2+2.7-3)=0 \Rightarrow x_1=0\\ x_2(1-p_1+2p_2)=0 \Rightarrow x_2(1-7+3.2)=0 \Rightarrow x_2\geq 0\\ x_3(4-p_1+p_2)=0 \Rightarrow x_3(4-7+3)=0\Rightarrow x_3\geq 0\end{align}  $$
obtemos o sistema $$\begin{pmatrix}7 & 7 \\ -6 & 3\end{pmatrix}\begin{pmatrix}x_2 \\ x_3\end{pmatrix}=\begin{pmatrix}7 \\ -3\end{pmatrix}$$
e finalizamos com $x^*=\begin{pmatrix}0 & 2/3 & 1/3\end{pmatrix}^t$

<mark style="background: #FFB86CA6;">Para</mark>
$\begin{align}\min z=2x_1+3x_2+5x_3+2x_4+3x_5\\ s.a:\begin{cases} x_1+x_2+2x_3+x_4+3x_5\geq 4\\ 2x_1-2x_2+3x_3+x_4+x_5\geq 3\\ x_i\geq 0, i=1,2,...,5\end{cases}\end{align}$ 

$\begin{align}\max 4p_1+3p_2\\ \begin{cases}p_1+2p_2\leq 2\\ p_1-2p_2\leq 3\\ 2p_1+3p_2 \leq 2\\ 3p_1 +p_2 \leq 3\\ \text{p livre}\end{cases}\end{align}$

```functionplot
---
title: Região
disableZoom: false
bounds: [-4,9,-4,9]
grid: true
xLabel: x
yLabel: y
---

f(x) = (2-x)/2
g(x) = (-3+x)/2
h(x) = (2-2*x)/3
i(x) = (3-3*x)

```
temos a [[Resolução gráfica]] com $p^*=\begin{pmatrix}-2 & 2\end{pmatrix}$

assim, 
$$\begin{align}p_1(x_1+x_2+2x_3+x_4+3x_5-4)=0\\ p_2(2x_1-2x_2+3x_3+x_4+x_5-3)=0\\ x_1(2-p_1-2p_2)=0\Rightarrow x_1(2+2-4)=0\Rightarrow x_1\geq 0\\ x_2(3-p_1+2p_2)=0\Rightarrow x_2(3+2+4)=0\Rightarrow x_2=0\\ x_3(2-2p_1-3p_2)=0\Rightarrow x_3(2+4-6)=0 \Rightarrow x_3\geq 0\\ x_4(3-3p_1-p_2)=0\Rightarrow x_4(3+6-2)=0\Rightarrow x_4=0\end{align}$$
temos então
$$\begin{align}-2x_1-4x_3=-8\\ 4x_1+6x_3=6\end{align}$$
e finalizamos com $x^*=\begin{pmatrix}-6 & 0 & 5 & 0\end{pmatrix}$
