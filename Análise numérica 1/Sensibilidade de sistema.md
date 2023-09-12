Considere o sistema $\displaystyle Ax=b$, A não singular , $b \neq 0$. Então o sistema tem solução única, a qual não é o vetor nulo.
Agora vamos "Perturbar um pouco" o vetor b por $\delta b$ 
	O sistema Perturbado é:
	$$\large \displaystyle A \hat x = b+\delta b$$
	que também tem solução única, esperamos que $\hat x$ não esteja "Muito longe" de x. Seja $\hat x = x + \delta x$.
Gostariamos que $\displaystyle \frac{||\delta b||}{||b||}$ "pequeno" implicasse $\displaystyle \frac{||\delta x||}{||X||}$ também pequeno
Veja que:
$\displaystyle A \hat x = b + \delta b$ => $\displaystyle A(X+\delta x) = b + \delta b$ => $\displaystyle Ax + A \delta x = b + \delta b$ 
=> $\displaystyle A \delta x = \delta b$, aplicamos $\displaystyle \delta x = A^{-1}\delta b$
$\displaystyle ||\delta x|| = ||A^{-1}\delta b|| \leq ||A^{-1}||.||\delta b||$
$$\displaystyle \large \frac{||\delta x||}{||A||.||x||} \leq \frac{||A^{-1}||.||\delta b||}{||b||} ~~\Rightarrow ~~\frac{||\delta x||}{||x||} \leq ||A||.||A^{-1}||. \frac{||\delta b||}{||b||}$$

- Denotamos $||A||.||A^{-1}||$ como [[Número de condição]] da [[Matriz]] A, $K(A)=||A||.||A^{-1}||$
1) Se K(A) não é "Muito grande", então $\displaystyle \frac{||\delta b||}{||b||}$ será "Bem pequeno" implica que $\displaystyle \frac{||\delta x||}{||x||}$ também o será
2) Se K(A) não é demasiadamente grande, dizemos que A é bem condicionada.
3) Se K(A) é demasiadamente grande dizemos que A é mal condicionada

**Exemplo**
- $A = \begin{pmatrix} 1000 & 999 \\ 999 & 998\end{pmatrix}$ => $\begin{pmatrix} -998 & 999 \\ 999 & -1000\end{pmatrix}$ $||A||_1 = ||A||_\infty = 1999 = ||A^{-1}||_\infty=||A^{-1}||_1$
	Obtemos K(A) = 1999.1999 $\approx 3.996.10^6$ ... A é mal condicionada
- Observe que ,
	$A\begin{bmatrix} 1 \\1\end{bmatrix} = \begin{bmatrix} 1999 \\1997\end{bmatrix}$, Vamos resolver o sistema
	$\begin{cases} 1000x_1 + 999x_2 = 1999\\ 999x_1 + 998x_2 = 1997\end{cases}$, A solução é : $\begin{bmatrix} 1 \\1\end{bmatrix}$  
	
	Agora pertubaremos levemente,
	$\begin{cases} 1000\hat x_1 + 999\hat x_2 = 1998.99\\ 999\hat x_1 + 998\hat x_2 = 1997.01\end{cases}$ => $\delta b = \begin{bmatrix} -0.01 \\0.01\end{bmatrix}$  e a solução é $\hat x = \begin{bmatrix} 20.97 \\-18.99 \end{bmatrix}$=> $\delta x = \begin{bmatrix} 19,97 \\-19.99\end{bmatrix}$ 
	