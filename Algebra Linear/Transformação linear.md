w = F(x); x é um vetor $\mathbb{R}^n$; w é um vetor em $\mathbb{R}^n$ 
f:$\mathbb{R}^n \rightarrow \mathbb{r}^m$


[[Transformação nula]]
- Leva um vetor até um vetor nulo

i. T(u+v) = T(u) + T(v)
ii. T($\alpha u$) = $\alpha T(u), ~ \forall \alpha \in \mathbb{R}, ~ \forall u \in V$

**Exemplo:**
T:$P_2 \rightarrow P_1$
T($a_0 + a_1x + a_2x^2$) = $(a_0+a_1)-(2a_1+3a_2)x$
Base canônica
$C_1(1,1,1)+C_2(1,1,0)+C_3(1,0,0)$
 
$\begin{bmatrix} C_1&C_1&C_1\\ C_2&C_2& &\\ C_3& & &\\ \end{bmatrix}\begin{bmatrix} x_1 \\ x_2 \\ x_3\end{bmatrix}$   -> $\begin{cases} c_2 = x_3\\c_2 = x_2-(x_1+x_2) = -x_1\\ c_1 = -(x_1+x_2x_3)+x_1 = x_2+x_3\end{cases}$


T:$\mathbb{R}_3 \rightarrow \mathbb{R}_2$ ... $T_{(2,3)}$
T(1,x, $x^2$)  = T(1,0,0)+ T$(0,x,0)$ + T$(0,0,x^2)$

$T(1,0,0) = (1+0) -(2.0 + 3.0) = 1+0x$
$T(0,x,0) = (0+1) - (2.1+3.0)x = 1-2x$
$T(0,0,x^2) = (0+0)-(2.0 +3.1)x = 0-3x$

e obtemos

$\begin{bmatrix} 1 & 1 & 0\\ 0 & -2& -3\end{bmatrix}$

