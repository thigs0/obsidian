Transformamos varias equações em um [[Sistema linear]] com notação de [[Geometria Analítica/Matriz]]
Problema: dois recipientes conectados por dois tubos
A-> primeiro tanque[
B -> Segundo tanque

A - $r_1$ 2 l/s , capacidade de 10l, entrada 2
B - 

x(t) = Quantidade de sal no tempo t em $r_1$
y(t) = Quantidade de sal no tempo t em $r_2$

x'(t) = $\displaystyle -\frac{3}{10}+ 1. \frac{y}{20}$
y'(t) = $\displaystyle 3\frac{x}{10} - \frac{y}{20} - \frac{2y}{20}$ E temos um sistema para resolver

**Para o sistema [[Massa-mola]]**
Parede- mola 1- massa - mola 2- massa - livre
$m_1 x''(t) = -k_1x(t)+k_2(y(t)-x(t))$
$m_2y''(t) = -k_2(y(t)-x(t)+f(t))$ 


**De modo geral** 
$x_1'(t) = P_{11}(t)x_1 + P_{12}(t)x_2+...+ P_{1n}(t)x_n$ + $f_1(t)$
$x_2'(t) = P_{21}(t)x_1 + P_{22}(t)x_2+...+ P_{2n}(t)x_n$ + $f_2(t)$
...      ...   ...    ... ...  + ...
$x_n'(t) = P_{n1}(t)x_1 + P_{n2}(t)x_2+...+ P_{nn}(t)x_n$ $f_n(t)$

[[EDO]] de ordem n
	$x^{(n)} = f(t,x,x^{(1)}), x^{(2)}), x^{(3)}),...,x^{(n)})$
	e podemos reduzir à um sistema 
	Introduzir funções $x_i(t)$
	$x_1(t) = x(t)$ -> $x_1'(t) = x^{(1)}(t) = x_2(t)$
	$x_2(t) = x^{(1)}(t)$ -> $x_2'(t) = x^{(2)}(t) = x_3(t)$
	$x_3(t) = x^{(2)}(t)$ -> $x_3'(t) = x^{(3)}(t) = x_4(t)$
	... -> ...
	$x_n(t) = x^{(n-1)}(t)$ -> $x_n'(t) = x^{(n)}(t) = f(t)$
	Desta forma obtemos  $x_n'(t) = x^{(n)}(t) = f(t,x_1,...x_n)$ é um sistema de n equações de primeira ordem 
**teorema de existência e unicidade para sistemas**
	Se $P_{ij}(t)$ce $f_i(t)$ são contínuas no intervalo I aberto então dados $b_1, b_2, ... b_n$ existe solução única satisfazendo
	$y_(a) = b$, $y'(a) = b_2$, ... $y^{(n-1)}(a) = b_n$


*Exemplo*
	
	$\begin{cases} x' = x+2y \\ y' = 2x+y+\end{cases}$
	$x' = \begin{pmatrix}1 & 2 \\ 2 & 1 \end{pmatrix}x$ 
	1. Olhar para o [[Determinante]] de A
	$|| A-\lambda I = \begin{vmatrix}1-\lambda & 2 \\ 2 & 1-\lambda \end{vmatrix}=0$ -> $(1-\lambda)^2 -4=0 = \lambda^2-2\lambda -3$
	Então as raízes são
	$\begin{cases}\lambda =3 \\ \lambda =-1\end{cases}$
	2. Encontramos os autovetores
	(A-3I)V= 0 -> $2v_1-2v_2=0$ -> $V = \begin{pmatrix} 1 \\ 1\end{pmatrix}$
	(A-I)V = 0 -> $\begin{pmatrix} 2 & 2\\ 2 &2\end{pmatrix}V=0$ -> $2v_1+2v_2=0$ -> $V = \begin{pmatrix}1 \\-1\end{pmatrix}$ 
	-
	A solução é X' = $c_1 e^{3t}\begin{pmatrix}1 \\-1\end{pmatrix} + c_2e^{-1t}\begin{pmatrix}1 \\ -1\end{pmatrix}$ 
	$\begin{pmatrix}x(t) \\y(t)\end{pmatrix} = \begin{pmatrix}c_1 e^{-t}+c_2 e^{-t}\\ c_1e^{3t} - c_2e^{-t}\end{pmatrix}$
	


**Para autovalor complexo**

**Para autovalor repetido**


