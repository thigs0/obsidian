![[O algoritmo dual simplex.pdf]]


**Exemplo**
$\begin{align}\min f(x)=2x_1+3x_2+4x_3\\ \begin{cases}x_1+2x_2+x_3\geq 3\\ 2x_1-x_2+3x_3\geq 4\\ x\geq 0\end{cases}\end{align}\hspace{1cm}$ $\begin{align}\max g(\lambda) =3\lambda_1+4\lambda_2\\ \begin{cases} \lambda_1+\lambda_2\leq 2\\ 2\lambda_1-\lambda_2\leq 3\\ \lambda_1+3\lambda_2\leq 4\\ \lambda \geq 0\end{cases}\end{align}$

*Forma padrão*

**1º Iteração**
*Fase 1*
Solução básica dual factível

$\lambda_1=0$, $\lambda_2=0$ é uma solução dual factível pois satisfaz todas as restrições do problema dual
$\hat \lambda = \begin{pmatrix}0 \\ 0\end{pmatrix}$, $A=\begin{pmatrix}1 & 2 & 1 & -1 & 0 \\ 2 & -1 & 3 & 0 & -1\end{pmatrix}$, $b=\begin{pmatrix}3 \\ 4\end{pmatrix}$ 

$B=\begin{pmatrix}a_4 & a_5\end{pmatrix}$, $x_b=\begin{pmatrix}x_4 \\ x_5\end{pmatrix}$, $x_N=\begin{pmatrix}x_1 \\ x_2 \\ x_3\end{pmatrix}$, $N=\begin{pmatrix}a_1 & a_2 & a_3\end{pmatrix}$,$c_B=\begin{pmatrix}0  \\ 0\end{pmatrix}$, $c_N=\begin{pmatrix}2 \\ 3 \\ 4\end{pmatrix}$ 
*Passo 1*: Solução  básica dual e custos relativos
- $B^t\lambda =C_B$ => $\begin{pmatrix}-1 & 0 \\ 0 & -1\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2\end{pmatrix}=\begin{pmatrix}0 \\ 0\end{pmatrix}$ => $\hat \lambda =\begin{pmatrix}0 \\ 0\end{pmatrix}$
-  $\hat C_{N_j}=C_{N_j}-\lambda^ta_{N_j}$ j=1,2,...,n-m
1) $\hat C_{N_1}=C_1-\begin{pmatrix}0 & 0\end{pmatrix}\begin{pmatrix}1 \\ 2\end{pmatrix}=2$
2) $\hat C_{N_2}=C_2-\begin{pmatrix}0 & 0\end{pmatrix}\begin{pmatrix}2 \\ -1\end{pmatrix}=3$
3) $\hat C_{N_3}=C_3-\begin{pmatrix}0 & 0\end{pmatrix}\begin{pmatrix}1 \\ 3\end{pmatrix}=4$

*Passo 2*: Teste de otimalidade
2.1) Solução básica primal $Bx_B=b$
$\begin{pmatrix}-1 & 0 \\ 0 & -1\end{pmatrix}\begin{pmatrix}x_4 \\ x_5\end{pmatrix}=\begin{pmatrix}3 \\ 4\end{pmatrix} \Rightarrow x_6=\begin{pmatrix}-3 \\ -4\end{pmatrix}$
2.2) 
$\min {-3,-4}=-4$, então $x_5$ sai da base

*Passo 3*: Calculo da direção si mplex
$B^t\eta_i=-e_i$
$\begin{pmatrix}-1 & 0 \\ 0 & -1\end{pmatrix}\begin{pmatrix}\eta_{2_1} \\ \eta_{2_2}\end{pmatrix}=\begin{pmatrix}0 \\ -1\end{pmatrix}\Rightarrow \eta_2 = \begin{pmatrix}0 \\ -1\end{pmatrix}$

*Passo 4*: Determinar tamanho do passo e variável a entrar na base
Se $\eta_e^ta_{N_j}\leq 0$; $j=1,2,...,n-m$ então pare, o problema é infactível
-> Caso contrário, determine

$\displaystyle \hat \delta=\frac{\hat c_{N_k}}{\eta_2^t a_{N_k}}=\min_j \left\{\frac{\hat c_{N_1}}{\eta_2^t a_{N_j}}/\eta_2^t a_{\mu_j}>0 \right\}$   
$\eta_2^ta_{N_1}=\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}1 \\ 2\end{pmatrix}=2$
$\eta_2^ta_{N_2}=\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}2 \\ -1\end{pmatrix}$
$\eta_2^ta_{N_3}=\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}1 \\ 3\end{pmatrix}=3$
$\sigma = \min \left\{ \frac{2}{2};\frac{4}{3}\right\}$ => $N_1$ entra na base
 *Passo 5*:Atualiza
 $B=\begin{pmatrix}-1 & 1 \\ 0 & 2\end{pmatrix}, =\begin{pmatrix}a_4 & a_1\end{pmatrix}$ ; $N=\begin{pmatrix}a_5 & a_2 & a_3\end{pmatrix}$; $x_B=\begin{pmatrix}x_4 \\ x_1\end{pmatrix}$; $x_N=\begin{pmatrix}x_5 \\ x_2 \\ x_3\end{pmatrix}$; $c_B=\begin{pmatrix}0 \\ 2\end{pmatrix}$; $c_N=\begin{pmatrix}0 \\ 3 \\ 4\end{pmatrix}$
**2° Iteração**
*1º passo*
$B^t\lambda =c_B$ => $\begin{pmatrix}-1 & 0 \\ 1 & 2\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2\end{pmatrix}=\begin{pmatrix}0 \\ 2\end{pmatrix}$ => $\lambda=\begin{pmatrix}0 \\ 1\end{pmatrix}$
$\begin{align} \hat c_{N_1} = c_{N_1} -\lambda^ta_{M_1}=0-\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}0 \\ -1\end{pmatrix}=1\\ \hat c_{N_2} =c_{N_2}-\lambda^ta_{N_2}=3-\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}2 \\ -1\end{pmatrix}=4\\ \hat c_{N_3}=c_{N_3}-\lambda^ta_{N_3}=4-\begin{pmatrix}0 & 1\end{pmatrix}\begin{pmatrix}1 \\ 3\end{pmatrix}=1 \end{align}$
*2° Passo*
$B\hat x_B =b$ => $\begin{pmatrix}-1 & 1 \\ 0 & 2\end{pmatrix}\begin{pmatrix}\hat x_1 \\ \hat x_2\end{pmatrix}=\begin{pmatrix}3 \\ 4\end{pmatrix}$ => $\hat x=\begin{pmatrix}-1 \\ 2\end{pmatrix}$
*3º passo*
$B^t\eta =-e$  => $\begin{pmatrix}-1 & 0 \\ 1 & 2\end{pmatrix}\begin{pmatrix}\eta_1 \\ \eta_2\end{pmatrix}=\begin{pmatrix}-1 \\ 0\end{pmatrix}$ => $\eta =\begin{pmatrix}1 \\ 1/2\end{pmatrix}$
*4° Passo*
$\begin{align} \eta^ta_{N_1}=\begin{pmatrix}1 & 1/2\end{pmatrix}\begin{pmatrix}0 \\ -1\end{pmatrix} =-1/2 \\ \eta^t a_{N_2}=\begin{pmatrix}1 & 1/2\end{pmatrix}\begin{pmatrix}2 \\ -1\end{pmatrix}=3/2\\ \eta^ta_{N_3}=\begin{pmatrix}1 & 1/2\end{pmatrix}\begin{pmatrix}1 \\ 3\end{pmatrix}=5/2\end{align}$
$\sigma = \min \{ \frac{3}{3/2} = 2; \frac{4}{5/2}=\frac{8}{5}\}=\frac{8}{5}$
$N_3$ entra na base
*5° Passo*
$A=\begin{pmatrix}1 & 2 & 1 & -1 & 0 \\ 2 & -1 & 3 & 0 & -1\end{pmatrix}$ $B=\begin{pmatrix}1 & 1 \\ 3 & 2\end{pmatrix},=\begin{pmatrix}a_3 & a_1\end{pmatrix}$; $N=\begin{pmatrix}a_5 & a_2 & a_4\end{pmatrix}$; $x_B=\begin{pmatrix}a_3 \\ a_1\end{pmatrix}$; $x_N=\begin{pmatrix}x_5 \\ x_2 \\ x_4\end{pmatrix}$; $c_B=\begin{pmatrix}4 \\ 2\end{pmatrix}$; $C_N=\begin{pmatrix}0 \\ 3 \\ 0\end{pmatrix}$
**3° Iteração**
*1º Passo*
$B^t\lambda =c_B$ => $\begin{pmatrix}1 & 3 \\ 1 & 2\end{pmatrix}\begin{pmatrix}\lambda_1 \\ \lambda_2\end{pmatrix}=\begin{pmatrix}4 \\ 2\end{pmatrix}$ => $\lambda =\begin{pmatrix}-2 \\ 2\end{pmatrix}$
*2º Passo*
$B\hat x_B=b$=> $\begin{pmatrix}1 & 1 \\ 3 & 2\end{pmatrix}\begin{pmatrix}\hat x_1  \\ \hat x_2\end{pmatrix}=\begin{pmatrix}3 \\ 4\end{pmatrix}$ => $\hat x=\begin{pmatrix}-2 \\ 5\end{pmatrix}$
*3º Passo*
$B^t\eta =-e$ => $\begin{pmatrix}1 & 3 \\ 1 & 2\end{pmatrix}\begin{pmatrix}\eta_1 \\ \eta_2\end{pmatrix}=\begin{pmatrix}-1 \\ 0\end{pmatrix}$ => $\eta =\begin{pmatrix}2 \\ -1\end{pmatrix}$
*4º Passo*
$\begin{align} \eta^ta_{N_1}=\begin{pmatrix}2 & -1\end{pmatrix}\begin{pmatrix}0 \\ -1\end{pmatrix}=1\\ \eta^t a_{N_2} = \begin{pmatrix}2 & -1\end{pmatrix}\begin{pmatrix}2 \\ -1\end{pmatrix}=5\\ \eta^ta_{N_2}=\begin{pmatrix}2 & -1\end{pmatrix}\begin{pmatrix}-1 \\ 0\end{pmatrix}=-2\end{align}$
$\sigma =\min \{ \frac{0}{1};\frac{3}{5} \}=0$, $N_1$ entra na base
*5º Passo*
$A=\begin{pmatrix}1 & 2 & 1 & -1 & 0 \\ 2 & -1 & 3 & 0 & -1\end{pmatrix}$ ;$B=\begin{pmatrix}0 & 1 \\ -1 & 2\end{pmatrix},=\begin{pmatrix}a_5 & a_1\end{pmatrix}$; $N=\begin{pmatrix}a_3 & a_2 & a_4\end{pmatrix}$; $x_B=\begin{pmatrix}x_5 \\ x_1\end{pmatrix}$; $x_N=\begin{pmatrix}x_3 \\ x_2 \\ x_4\end{pmatrix}$; $c_B=\begin{pmatrix}0 \\ 2\end{pmatrix}$; $c_N=\begin{pmatrix}4 \\ 3 \\ 0\end{pmatrix}$
**IV Iteração**
*1º Passo*
$B^t\lambda =c_B$ => $\begin{pmatrix}0 & -1 \\ 1 & 2\end{pmatrix}\begin{pmatrix}\lambda_1  \\ \lambda_2 \end{pmatrix}=\begin{pmatrix}0 \\ 2\end{pmatrix}$

*2º Passo*
$B\hat x_B=b$ => $\begin{pmatrix}0 & 1 \\ -1 & 2\end{pmatrix}\begin{pmatrix}\hat x_1 \\ \hat x_2\end{pmatrix}=\begin{pmatrix}3 \\ 4\end{pmatrix}$ => $\hat x=\begin{pmatrix}2 \\ 3\end{pmatrix}$

Como $\hat x >0$, estamos em um ótimo
$x=\begin{pmatrix}3 \\ 0 \\ 0\end{pmatrix}$ com $f(x)=6$
$\lambda = \begin{pmatrix}2 \\ 0\end{pmatrix}$ com $g(\lambda)=6$
