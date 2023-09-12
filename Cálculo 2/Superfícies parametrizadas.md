- Parametrizar uma curva permite representar um objeto de $R^3$->$R^2$ 

Uma equação parametrizada é de forma $\displaystyle \large R(x(u,v),y(u,v)) = x(u,v)\hat i+y(u,v)\hat j+ z(u,v)\hat k$ 

Em geral uma superfície de forma $X=X;~~~~Y=Y;~~~~~Z=f(x,y)$ Pode ser parametrizada tomando cada termo como parâmetro


- ### [[Superfície de revolução]]
	As superfícies de revolução podem ser parametrizadas por apresentarem simetria axial


- ### [[Plano tangente]]
	O plano tangente é o plano que toca a função em um ponto $(u_0,v_0)$ 

	Como sabemos que a [[Derivada]] parcial de R em relação a u e v está no plano tangente. O produto vetorial entre ambos será o vetor normal ao plano
	$\vec R_u \times \vec R_v = \vec N$
	Se o vetor normal é o vetor nulo, a curva não é suave
	Assim o plano tangente em uma superfície parametrizada tem forma$$<\vec R_u \times \vec R_v~, (x-x_0,y-y_0,z-z_0)>~=0$$
- ### área da superfície
	Uma aproximação para área de pequenos retângulos é $\displaystyle \sum_{i=1}^m \sum_{j=1}^n |\vec R_u \times \vec R_v|\Delta u \Delta v$ 
	De modo que obtemos a definição:

	$$A(S)= \iint_D |\vec r_u \times \vec r_v|dA$$
	