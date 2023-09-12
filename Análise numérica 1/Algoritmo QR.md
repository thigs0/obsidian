- Leva este nome por usar a [[Decomposição QR]]
- Um dos mais usados para calcula [[Autovalor]]es 
Considere a [[Matriz]] $\mathbb{R}^{nxn}$. Suponhamos que A é não singular. O algoritmo QR é 
Inicialize $A_0=A$ 
Gere a sequência:
$A_{m-1}=Q_mR_m$
$A_m=R_mQ_m$  

Onde $Q_m$ é uma matriz unitária, $R_m$ é uma matriz triangular superior com as entradas da diagonal positiva

**Obs**
	1. $A_m=Q_m^tA_{m-1}Q_m$, com $Q^t=Q^{-1}$, ou seja $A_m$ e $A_{m-1}$ são similares. Portanto, possuem os mesmos [[Autovalor]]res 
	2. Deve-se ter atenção que decomposição QR é diferente de algoritmo QR. O algoritmo QR é um método iterativo para determinar autovalores. Uma iteração do algoritmo QR será chamado de passo QR ou iteração QR.

**Exemplo**
Aplique o algoritmo QR a matriz $$A=\begin{pmatrix}8 & 2 \\ 2 & 5\end{pmatrix}$$
Que é simétrica (os autovalores são 9 e 4)
$A_0=A$
$Q= \begin{pmatrix}c & -s \\ s & c\end{pmatrix}$
$\displaystyle c=\frac{8}{\sqrt{8^2+2^2}}=\frac{8}{\sqrt{68}}$, $\displaystyle s=\frac{2}{\sqrt{8^2+2^2}}=\frac{2}{\sqrt{68}}$ 
Encontramos o R.
$\displaystyle R=Q^tA=\frac{1}{\sqrt{68}}\begin{pmatrix}8 & 2 \\ -2 & 8\end{pmatrix}\begin{pmatrix}8 & 2 \\ 2 & 5\end{pmatrix}=\frac{1}{\sqrt{68}}\begin{pmatrix}68 & 26 \\ 0 & 36\end{pmatrix}$ 
Encontramos o $A_1$ de modo
$\displaystyle A_1=RQ=\frac{1}{\sqrt{68}}\begin{pmatrix}68 & 26 \\ 0 & 36\end{pmatrix}.\frac{1}{\sqrt{68}}\begin{pmatrix}8 & -2 \\ 2 & 8\end{pmatrix}=\frac{1}{68}\begin{pmatrix}596 & 72 \\ 72 & 288\end{pmatrix}$ 

$Q= \begin{pmatrix}c & -s \\ s & c\end{pmatrix}$ 
$\displaystyle c=\frac{596/68}{\sqrt{(596/8)^2+(72/8)^2}}=8.8284$, $s=0.1199$
$R=\begin{pmatrix}8.8284 & 1.5591 \\ 0 & 4.0777\end{pmatrix}$
Então 
$A_2=RQ=\begin{pmatrix}8.9517 & 0.491 \\ 0.48891 & 4.0483\end{pmatrix}$
.
.
.
Até i=20. Obtemos
$A_{20}=\begin{pmatrix}9.0 & 2.2*10^{-7} \\ 2.2*10^{-7} & 4.0\end{pmatrix}$ Observe que A também é simétrica


---
###### **Teorema**
Seja $A_{m-1}$ uma [[Matriz de Hessemberg]] superior, não singular. Suponha $A_m$ é obtida de $A_{m-1}$ por passo QR. Então $A_m$ também será matriz de Hessemberg superior.
***Exemplo***
$A=\begin{pmatrix}1 & 2 & -1 \\ 1 & 2 & 2 \\ 0 & 3 & 4\end{pmatrix}$ => $Q=\begin{pmatrix}-0.70711 & 0 & 0.70711 \\ -0.70711 & 0 & -0.70711 \\ 0 & -1 & 0\end{pmatrix}$, $r=\begin{pmatrix}-1.41421 & -2.82843 & -0.7071 \\ 0 & -3 & -4 \\ 0 & 0 & -2.121\end{pmatrix}$
$A_1=RQ=\begin{pmatrix}3.0 & 0.70711 & 1 \\ 2.12132 & 4 & 2.12132 \\ 0 & 2.12132 & 0\end{pmatrix}$
Que é Hessenberg superior

Caso Pegássemos uma matriz singular
$A=\begin{pmatrix}0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{pmatrix}$ Que é [[Matriz de Hessemberg]]
Então $Q=\begin{pmatrix}0 & 0 & 1 \\ 0  & 1 & 0 \\ 1 & 0 & 0\end{pmatrix}$ e $R=\begin{pmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{pmatrix}$
e $A_1=\begin{pmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0\end{pmatrix}$ que não é uma [[Matriz de Hessemberg]]
