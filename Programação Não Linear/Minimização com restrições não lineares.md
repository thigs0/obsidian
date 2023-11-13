**Condições de 1ºordem**
x é [[Minimizador]] local regular => $\exists ! \lambda^* \in \mathbb{R}^m$
$\nabla f(x^*)+\sum_{i=1}^m \lambda_i^* \nabla h_i(x^*)=0 \Leftrightarrow \nabla f(x^*)+J_h(x^*)^t\lambda^*$
sendo $J_h(x^*)$ o [[Jacobiana]] no ponto $x^*$
![[nlinear_equal.png|400]]
$$J_h(x)=\begin{pmatrix}\nabla h_1(x)^t \\ \nabla h_2(x)^t \\ ... \\ \nabla h_2(x)^t\end{pmatrix} \in \mathbb{R}^{m\times n}$$



$$\boxed{\begin{align}\min f(x)\\ \begin{cases} g_1(x)\leq 0\\ g_2(x)\leq 0\\ g_3(x)\leq 0\\ ...\\g_p(x)\leq 0\end{cases}\end{align} \hspace{2cm}f,g:\mathbb{R}^n\rightarrow \mathbb{R},i=1,2,3,...,p; f,g\in c^2}$$
![[nlinear_desigual.png|400]]
**CN1** 
$x^*$ é um [[Minimizador]] local regular 
$$\exists !\mu^* \in \mathbb{R}^p_+, \nabla f(x^*)+\sum_{j=1}^p \nabla g_j(x^*)\mu^*=0$$
**CN2**
$x^*$ é um [[Minimizador]] local regular => $\exists ! \lambda^* \in \mathbb{R}^m$,
1) $\nabla f(x^*) +\sum_{i=1}^m \lambda_i^* \nabla h_i(x^*) =0$
2) $y^t[\nabla^2 f(x^*)+\sum_{i=1}^m \lambda_i^* \nabla^2h_i(x^*)]y \geq 0;\hspace{1cm} \forall y\in \mathscr{N}(J_k(x^*))$ 