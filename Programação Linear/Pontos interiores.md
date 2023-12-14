- O método consiste em caminhar pelo interior da região factível para o ótimo 
![[pontos_interiores_represent.png|400]]
- Métodos de pontos interiores, ao contrário dos métodos tipo simplex, usam a cada iteração toda a matriz de restrições, tornando o custo computacional por iteração bastante elevado. Porém, realiza um número menor de iterações (poucas dezenas).


**Interior**
$P' =\{ x \in \mathbb{R}^n/ Ax=b,x>0 \}$
$D'= \{ (p,s)\in \mathbb{R}^m \times \mathbb{R}^n/A^tp+s=c,s>0 \}$

$\begin{align}\textbf{Problema primal}\\ \min f(x)=c^tx\\ s.a:\begin{cases}Ax\geq b\\ x\geq 0\end{cases}\end{align}$

pelas [[Condições KKT]]

$$\begin{align} Ax=b,~x\geq 0\\ A^tp+s=c,~s\geq 0\\ s_jx_j=0,~j=1,2,...,n \end{align}$$

**Notação**
$X=diag(x_1,x_2,...,x_n)$
$S=diag(s_1,s_2,...,s_n)$
$e=(1,1,...,1)^t$

e obtemos o sistema
$$\begin{align} Ax=b\\ A^tp+s=c\\ XSe=\delta e \end{align}$$

$F(x,p,s)=\begin{pmatrix}Ax-b \\ A^tp+s-c \\ XSe-\delta e\end{pmatrix}$

dado o ponto $(\bar x, \bar p, \bar s)$ temos a direção por
$\nabla F(\bar x,\bar p, \bar s)\begin{pmatrix}\Delta x\\ \Delta p\\ \Delta s\end{pmatrix}=-F(\bar x,\bar p,\bar s)$
sendo $\nabla F(\bar x, \bar p,\bar s)=\begin{pmatrix}\nabla_\times F_1 & \nabla_pF_1 & \nabla_SF_1 \\ \nabla_\times F_2 & \nabla_pF_2 & \nabla_SF_2 \\ \nabla_\times F_3 & \nabla_pF_3 & \nabla_SF_3\end{pmatrix}=\begin{pmatrix}A & 0 & 0 \\ 0 & A^t & I \\ \bar S & 0 & \bar X\end{pmatrix}$

$$\begin{pmatrix}A & 0 & 0 \\ 0 & A^t & I \\ \bar S & 0 & \bar X\end{pmatrix}\begin{pmatrix}\Delta x\\ \Delta p\\ \Delta s\end{pmatrix}=-\begin{pmatrix}A\bar x-b\\ A^t\bar p+\bar s-c\\ \bar X \bar S e-\delta e\end{pmatrix}$$

com atualização
$(x,p,s)=(\bar x,\bar p,\bar s)+\theta(\Delta x,\Delta p,\Delta s)$

**Tamanho do passo**

$\theta =\beta \min \{ 1; -\frac{\hat x_j}{\Delta x_j}/\Delta x_{j} <0; -\frac{\hat s_j}{\Delta s_j}/\Delta s_j<0 \}$

**Critério de parada**
$\rho_p =b-Ax^k \to 0$
$\rho_d^k =c-A^tp^k-s \to 0$ 
$\displaystyle \frac{(x^k)^ts^k}{n} \to 0$


**Algoritmo**
$\alpha:Float$
$\beta:Float$
$K_{max}$ <- Número máximo de iterações
$\tau_p>0;\tau_d>0;\tau_o>0$ <- Tolerâncias


