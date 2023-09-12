**Algoritmo**
![[Slide10.pdf]]

```julia
function Simplex(B, N, xb, cb, xn)
	#Solução básica
	xb = B\b
	xn = zeros(length(xn))
	f = cb'*xb #valor atual da função

	#Custos relativos
	λ = B'\cb
	cn = 
end
```

***Exemplo***
$\min f(x)=-3x_1-5x_2$
$s.a:\begin{cases}x_1 \leq 4// x_2 \leq 6 \\ 3x_1+2x_2\leq 18 \\ x_1\geq 0,x_2\geq 0\end{cases}$
Passamos para a forma padrão
$\min f(x)=-3x_1-5x_2$
$$s.a:\begin{cases}x_1  &  & x_3 &  &  & =4  \\
 & x_2 &  & x_4 &  & =6 \\
3x_1 & 2x_2 &  &  & x_5 & =18 \\
x_1\geq 0,x_2\geq 0,x_3\geq 0, x_4\geq5\end{cases}$$
De forma a $$A=\begin{pmatrix}1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 1 & 0 \\ 3 & 2 & 0 & 0 & 1\end{pmatrix};~~C=\begin{pmatrix}-3 \\ -5 \\ 0 \\ 0 \\ 0\end{pmatrix},~~~b=\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}$$
**Fase 1**
Encontrar uma partição básica factível
Tomamos a coluna $i$ como sendo $a_i$ $$B=\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix},~~N=\begin{pmatrix}1 & 0 \\ 0 & 1 \\ 3 & 2\end{pmatrix},~~C_N=\begin{pmatrix}-3 \\ -5\end{pmatrix}~~e~C_B=\begin{pmatrix}0 \\ 0 \\ 0\end{pmatrix}$$
**Fase 2**
Passo 1: Solução básica factível
$Bx_b=b$
$\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}x_3 \\ x_4 \\ x_5\end{pmatrix}=\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}\Rightarrow x_B=\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}\geq 0$ 
$f(\hat x_B)=C_B^tx_B=\begin{pmatrix}0 & 0 & 0\end{pmatrix}\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}=0$
Passo 2: 
- [[Vetor multiplicador simplex]] $B^t\lambda =C_b$
$\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2 \\ \lambda_3\end{pmatrix}=\begin{pmatrix}0 \\ 0 \\ 0\end{pmatrix}\Rightarrow \lambda =\begin{pmatrix}0 \\ 0 \\ 0\end{pmatrix}$
- [[Custo reduzido]] dos não básicos
$$j=1, \hat c_{N_1}=C_1-\lambda^{t}a_1=-3-\begin{pmatrix}0 & 0 & 0\end{pmatrix}\begin{pmatrix}1 \\ 0 \\ 3\end{pmatrix}=-3$$
$$j=2:C_{N_2}=C_2-\lambda^ta_2=-5\begin{pmatrix}0 & 0 & 0\end{pmatrix}\begin{pmatrix}1 \\ 0 \\ 3\end{pmatrix}=-5$$
K=2,
Passo 3:
Então $\hat C_{N_k}=\min \{C_{N_1}, C_{N_2}\}=C_{N_2}$
$x_2$ entra na base
Não estamos na sol ótima $c_j\leq 0$

Passo 4: [[Direção simplex]] $By=A_{N_k}$
$$\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}y_1 \\ y_2 \\ y_3\end{pmatrix}=\begin{pmatrix}0 \\ 1 \\ 2\end{pmatrix}\Rightarrow y=\begin{pmatrix}0 \\ 1 \\ 2\end{pmatrix}$$
Passo 5: Tamanho do passo
$\displaystyle \epsilon =\min_i \left\{ \frac{x_{B_i}}{y_i}|y_i>0 \right\}=6$ 
$x_{B_2}=x_4~\text{sai da base}$

Passo 6: Atualização da base
$B=\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 0 \\ 0 & 2 & 1\end{pmatrix},~N=\begin{pmatrix}1 & 0 \\ 0 & 1 \\ 3 & 0\end{pmatrix},~C_B^t=\begin{pmatrix}0 & -5 & 0\end{pmatrix},~C_N^t=\begin{pmatrix}-3 & 0\end{pmatrix}$ 

**2º Iteração**
Passo 1: Solução básica factível
$$\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 0 \\ 0 & 2 & 1\end{pmatrix}\begin{pmatrix}x_3 \\ x_2 \\ x_6\end{pmatrix}=\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}\Rightarrow x=\begin{pmatrix}4 \\ 6 \\ 6\end{pmatrix}\geq 0$$
$f(\hat x_B)=C_B^t\hat x=\begin{pmatrix}0 & -5 & 0\end{pmatrix}\begin{pmatrix}4 \\ 6 \\ 6\end{pmatrix}=-30$
Passo 2: Vetor multiplicador simplex $b^t\lambda =C_B$
$$\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 0 \\ 0 & 2 & 1\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2 \\ \lambda_3\end{pmatrix}=\begin{pmatrix}0 \\ -5 \\ 0\end{pmatrix}\Rightarrow\lambda=\begin{pmatrix}0 \\ -5 \\ 0\end{pmatrix}$$
- Custo reduzido
$j=1:\hat C_{N_1}=C_1-\lambda^ta_1=3$
$j=2:C_{N_2}=C_4-\lambda^ta_4=5$ 


Passo 3:
Então $\hat C_{N_k}=\min\{ C_{N_1},C_{N_2}\}=C_{N_1}$
$x_1$ entra na base
Não estamos na solução ótima $C_{N_j}<0$

Passo 4: Direção simplex $By=a_{N_k}$
$$\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 0 \\ 0 & 2 & 1\end{pmatrix}\begin{pmatrix}y_1 \\ y_2 \\ y_3\end{pmatrix}=\begin{pmatrix}1 \\ 0 \\ 3\end{pmatrix}\Rightarrow y=\begin{pmatrix}1 \\ 0 \\ 3\end{pmatrix}$$
Passo 5: Tamanho do passo
$\epsilon=\min_i \left\{ \frac{x_{B_i}}{y_i}|y_i>0\right\}=2$
$x_5$ sai da base

Passo 6: Atualiza a base
$B=\begin{pmatrix}1 & 0 & 1 \\ 0 & 1 & 2 \\ 0 & 2 & 3\end{pmatrix}$, $N=\begin{pmatrix}0 & 0 \\ 0 & 1 \\ 1 & 0\end{pmatrix}$ , $C_B^t=\begin{pmatrix}0 & -5 & -3\end{pmatrix}$, $C_N^t=\begin{pmatrix}0 & 0\end{pmatrix}$ 
**3º Iteração**
Passo 1: Achar a solução básica $B \hat x_B=b$ 
$\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 2 \\ 0 & 2 & 1\end{pmatrix}\begin{pmatrix}x_3 \\ x_2 \\ x_1\end{pmatrix}=\begin{pmatrix}4 \\ 6 \\ 18\end{pmatrix}\Rightarrow \hat x_B=\begin{pmatrix}2 \\ 6 \\ 2\end{pmatrix}\geq 0$ 
$f(\hat x_B)=C_B^t\hat x_B=\begin{pmatrix}0 & -5 & -3\end{pmatrix}\begin{pmatrix}2 \\ 6 \\ 2\end{pmatrix}=-36$ 
Passo 2:
- Vetor multiplicador simplex $B^t\lambda =C_B$ 
$$\begin{pmatrix} 1& 0 & 0 \\ 0 & 1 & 2 \\ 0 & 2 & 1\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2 \\ \lambda_3\end{pmatrix}=\begin{pmatrix}0 \\ -5 \\ -3\end{pmatrix}\Rightarrow \lambda=\begin{pmatrix}0 \\ -3 \\ -1\end{pmatrix}$$
- custos reduzidos 
$j=1:\hat C_{N_1}=C_5-\lambda^ta_5=0-\begin{pmatrix}0 & -3 & -1\end{pmatrix}\begin{pmatrix}0 \\ 0 \\ 1\end{pmatrix}=1\geq 0$
$j=2:\hat C_{N_2}=C_4-\lambda^t a_4=0-\begin{pmatrix}0 & -3 & -1\end{pmatrix}\begin{pmatrix}0 \\ 1 \\ 0\end{pmatrix}=3\geq 0$
Todos os custos reduzidos são $\geq 0$ , então estamos na solução ótima. A solução é
$$x^* =\begin{pmatrix}x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5\end{pmatrix}=\begin{pmatrix}2 \\ 6 \\ 2 \\ 0 \\ 0\end{pmatrix}~\text{Com } f(x^*)=-36$$




