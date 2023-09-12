- Usamos multiplicadores de lagrange para maximizar ou minimizar a distância até uma curva de nível

![[esfera.png]]

Exemplo: qual a menor distância entre a esfera e o centro de referência? 
A esfera é formada por varias circunferencia, então devemos achar a menor distância dessa circunferência até o contro

- Matemáticamente, multiplicadores de lagrange é $\lambda$ na equação:
$$\nabla f(x,y) = \lambda \nabla g(x,y)$$
f(x,y) é a função que queremos minimizar
g(x,y) é a função que contém os pontos de x e y
usamos a função [[Divergente]]

Muitas vezes, cairemos em um [[Sistema não linear]]

**Exemplo**
	Caixa de papelão de 12$m^2$, sem tampa. Qual o maior volume?
	$f = V =x.y.z$ volume
	g = 2xz+2yz+xy = 12 área
	$\begin{cases}yz = \lambda (2z+y)\\ xz = \lambda(2z+x)\\ xy = \lambda (2x+2y)\\ 2xy +2yz +xz = z\end{cases}$
	e temos a solução $\begin{bmatrix} 2\\2\\1\end{bmatrix}$
	
	