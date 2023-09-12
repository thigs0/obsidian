**Redução de ordem**
1. Caso: $F(x,y,y')=0$; Fazemos $v(x)= y'$
2. Caso: $F(y,y',y'')=0$; Fazemos $v(y(x)) =y'$
3. Presupõe conhecer uma solução

	$y_1^{''}+P(x)y_1^{'}+Q(x)y_1=0$
	criamos uma candidata a solução no formato $v(x)y_1(x)=y_2(x)$
	testamos a candidata: $\large \displaystyle \begin{cases}y_2'(x)= v'y_1'+vy_1'\\ y_2''(x)= v''y_1+vy_1'+ v'y_1'+vy_1''= v''y_1+2v'y_1'+vy_1''\end{cases}$
	Substituindo na equação: $\displaystyle v''y_1 +2v'y_1'+vy_1'' + P(x)[v'y_1+vy_1'] + Q(x)vy_1=0$
	Fatoramos o v: $\displaystyle v[y_1''+Py_1'+Qy_1]+ v''y_1 + v'[2y_1'+py_1] = v[0]+v''y_1 + v'[2y_1'+py_1]$
	Obtemos uma nova equação, de forma
	$\displaystyle W'y_1 + w[2y_1'+py_1]=0 \Rightarrow W'+ \frac{2y_1'+Py_1}{y_1}w=0$
	
	Podemos resolver por [[Equações separáveis]]
	$\large \displaystyle W = c_1 \frac{e^{-\int Pdx}}{y_1^2}$
	$\displaystyle v = \int c_2 \frac{e^{-\int Pdx}}{y_1^2} +C_2$
	
	_Exemplo_
	$\large x^2y''-x(x+2)y'+(x+2)y=0$ **e** $y_1=x$, para x>0
	1. Prove que $\large y_1$ é solução
	$\begin{cases}y_1 = x\\ y_1' = 1\\ y_1''=0 \end{cases}$; $x^2.0 -x(x+2).1+ (x+2)x = 0$

	Conseguindo outra solução
	$\begin{cases} y_2 = vx\\ y_2' = v'x+v\\ y_2''=v''x+2v'\end{cases}$
	
	Substituindo na equação
	$x³v''+2x²v'-(x²+2v)v'x-(x²+2x)v+ (x+2)vx=0$; os dois últimos termos cancelaram
	$x^3 v'' -x^3v' =0\Rightarrow  v''-v'=0$
	Criamos uma nova variável
	$\begin{cases} v'=W\\ v''=w'\end{cases}$ e obtemos: $W'-W=0$, resolvemos pelo método das separáveis e obtemos $y_2=C_2 xe^x + C_1x$
	
	
	
	