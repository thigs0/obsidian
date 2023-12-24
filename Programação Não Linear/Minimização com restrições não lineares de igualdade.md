$$ \begin{align} f:\mathbb{R}\to \mathbb{R},f\in C^2\\ h:\mathbb{R}^n\to \mathbb{R}^m~ h\in C^2 \end{align}\\ {dw}$$
$$\boxed{\begin{align}\min f(x) \\ s.a ~h(x)=0\end{align}}$$
sendo $h(x)=\begin{pmatrix}h_1(x)\\ h_2(x)\\...\\h_m(x)\end{pmatrix},\hspace{2cm} h:\mathbb{R}^n\to \mathbb{R}$  
**CN1**: Seja $x^*\in S$, [[Minimizador]] local e regular, ou seja, os [[Gradiente]]s $\nabla h_1(x^*),...,\nabla h_m(x^*)$ são [[Linear independente]]. Então existe um único $\lambda^*\in \mathbb{R}^m$, tal que 
$$\boxed{\nabla f (x^*)+\sum\limits_{i=1}^m \nabla h_i(x^*)\lambda_i^*=0}$$
**CS2**: $x^*\in S$, $\lambda^*\in \mathbb{R}^m,\mu^*\in\mathbb{R}_+^p$

1) $\nabla f(x^*)+A^t\lambda^*+W^t\mu^*=0$ com $\mu_j^*=0~se~W_j^tx^*<C_j$
2) $y^t\nabla^2 f(x^*) y>0$, $\forall 0\neq y\in \mathscr{N}\begin{pmatrix}A  \\ N_{F(x^*)}\end{pmatrix}$

