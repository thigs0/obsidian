Podemos construir uma função geral F
![[exemplo_rede.png]]

de modo que $F:\phi(Ax-b)$
assim, temos um vetor de dados $u$ e $v$ de forma que eles cada coordenada informa qual ponto do conjunto {-1, 1} estamos

por exemplo estes dados para treinar a rede
![[rede_treino.png|500]]
Queremos 
$$F= \frac{1}{N}\sum_{i=1}^N \frac{1}{2}(f(Ax-b)-w_i)^2$$
como $A\in \mathbb{R}^{2\times 2}$ e $b\in \mathbb{R}^2$ 

$u^1=\phi\left( \begin{pmatrix}x_1 & x_2 \\ x_3 & x_4\end{pmatrix}u+\begin{pmatrix}x_5 \\ x_6\end{pmatrix}\right)$
$v=\phi(\begin{pmatrix}x_7 & x_8\end{pmatrix}u^1+\begin{pmatrix}x_9\end{pmatrix})$
assim termos 9 parâmetros para ajustar $x\in \mathbb{R}^9$ 
como apresentado no [[Grafo]] abaixo
![[imagem/rede_simples.svg]]
assim
$$f(x, u) = \phi(\underbrace{x_7\phi(\underbrace{x_1u_1+x_2u_2+x_5}_{a_1})+x_8\phi(\underbrace{x_3u_1+x_4u_2+x_6}_{a_2})+x_9}_{a})$$
e o [[Gradiente]] é:
$$\nabla f = \begin{pmatrix}\phi'(a)x_7\phi'(a_1)u_1 \\ \phi'(a)x_7\phi'(a_1)u_1 \\ \phi'(a)x_8\phi'(a_2)u_1 \\ \phi'(a)x_8\phi'(a_2)u_2 \\ \phi'(a)x_7\phi'(a_1) \\ \phi'(a)x_8\phi'(a_2) \\ \phi'(a)\phi(a_1) \\ \phi'(a)\phi(a_2) \\ \phi'(a)\end{pmatrix}$$
sendo $\displaystyle \phi(t)=\frac{2}{\pi}\arctan(t)$ 

definimos 
```julia
function φ(t::int, flag::Int=0)
	a = 0.5*π;
	f = a*arctan(t)
	g = a/(1*t*t)
	if flag == 0
		return f
	else if flag ==1
		return (f, g)
	else
		return g
	end
end

function f(x::Vector, u::Vector)
	a1 = x[1]*u[1] + x[2]*u[2] + x[5]
	b2,c1 = φ(a1)
	a2 = x[3]*u[1]+x[4]*u[2]+x[6];
	b2,c2 = φ(a2)
	a = x[7]*b1 + x[8]*b2*x[9];
	b,c = φ(a);
	f=b;
	g = zeros(9)
	g[1] = x[7]*c1*u[1];
	g[2] = x[7]*c1*u[2];
	g[3] = x[8]*c2*u[1];
	g[4] = x[8]*c2*u[2];
	g[5] = x[7]*c1;
	g[6] = x[8]*c2;
	g[7] = b1;
	g[8] = b2;
	g[9] = 2
	g = c*g
	return f,g
end

function F(x::Vector, flag::int=0)
	global u; global v;m = length(x);
	f=0; g=0;
	for j in 1:m
		a,b = f(x, u[i,:]);
		aux = a-v[j];
		f += aux*aux;
		g += aux*b;
	end
	if flag==0
		return (f,g);
	else if flag == 1
		return f;
	else
		return g;
	end
end

```



