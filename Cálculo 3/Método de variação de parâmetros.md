Funciona para qualquer equação de ordem n na forma
$y{(n)}+ f(x)y{(n-1)}+...+f_n(x)y' = g(x)$

1. Determinar a solução da equação homogêna associada $y_c = c_1y_1 +c_2y_2+...+c_ny_n$
2 Supomos que a solução particular é de forma $y_p = u_1 (x)y_1 + y_1 + u_2(x)y_2+...+u_ny_n$, que satisfaça a equação

- **Ordem 2**
- $y'' +p(x)y' +q(x)y = f(x)$

	A solução complementar é $C_1 y_1+ C_2 y_2$
	propomos que a solução particular é $y_p = u_1y_1+u_2y_2$ 

$y_p' = u_1'y_1+u_2'y_2+u_1y_1'+u_2y_2'$ , impomos que $u_1'y_1+u_2'y_2 =0$
$y_p'' = u_1'y_1'+u_2'y_2' +u_1y_1''+u_2y_2''$ ; Com estas funções, aplicamos na equação

$u_1(y_1''+ p(x)y_1' +q(x)y_1')+u_2(y_2''+p(x)y_2'+q(x)y_2) = f(x)$; os termos dentro de $u_1$ se anulam

$\large \begin{cases} u_1' y_1 + u_2'y_2=0 \\ u_1'y_1' + u_2'y_2' = f(x)\end{cases}$ 

$\displaystyle u_1' = \frac{\begin{vmatrix} 0 & y_2 \\ f(x) & y_2'\end{vmatrix}}{W} = \frac{f(x)\begin{vmatrix} 0 & y_2 \\ 1 y_2'\end{vmatrix}}{W}$ 
$\displaystyle u_2' = \frac{\begin{vmatrix} y_1 & 0 \\ y_1' & f(x)\end{vmatrix}}{W}= \frac{f(x) \begin{vmatrix} y_1 & 0 \\ y_1' & 1\end{vmatrix}}{W}$


_Exemplo_
$x^2y'' -3xy'+4y=x^4$
1º) $x^2y'' -xy' + 4y=0$, e pela resolução de [[Equação de Euler-Cauchy]] temos a solução como:   $y_c = c_1x^2 +c_2x^2 \ln x$
2º) $y_p = u_1x^2+u_2 x^2 \ln x$ 