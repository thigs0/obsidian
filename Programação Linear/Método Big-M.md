Este método é uma alternativa para encontrar uma [[Solução básica]] inicial para o problema de programação linear

$A=\begin{bmatrix}B& N\end{bmatrix}$   

- a ideia é introduzir uma função custo da forma
$$\sum_{j=1}^nc_jx_j+M\sum\limits_{i=1}^m y_i$$
em que 
$M$ é uma constante positiva de valor grande
$y_i$ são as mesmas variáveis artificiais como na fase 1 do  método das duas fases

- Assim , no método do Big-M analisamos as variáveis artificiais no problema original

$Resolver$
$\min z=x_1-x_2+2x_3$
$s.a:\begin{cases}x_1+x_2\geq 3\\ -x_1+x_2\leq 1\\ x_j\geq 0\end{cases}$  