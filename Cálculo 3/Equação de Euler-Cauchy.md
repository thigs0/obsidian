Euler-Cauchy é de forma
$$x^ny^{(n)}+ a_{n-1}x^{n-1}y^{(n-1)}+...+a_1xy^{(1)}+a_0y$$

Candidata a equação de Euler-Cauchy é $f(x)=x^r$
substituindo dentro da equação
$x^r[r(r-1)....r-(n-1)+ a_{n-1}r(r-1)(r-(n-2))+...+a_1r+a_0]$
temos n raízes

1. Se as raízes são distintas
2. Raízes complexas
	$\large \displaystyle x^{a+ib}= x^ax^{ib} = e^{\ln [x^ax^{ib}]}=  e^{\ln [x^a]+\ln [x^{ib}]}= e^{\ln [x^a]}e^{\ln [ib]} = x^ae^{ib \ln (x)}$ usamos a [[Fórmula de Euler]]
	$x^a [\cos (b\ln x)+ \sin (b \ln x)]$
	_Exemplo_ 
	x²y''+7xy'+25y=0
	$y = x^r$
	$x^2[r(r-1)x^{r-2}+7x(rx^{r-1})+25x^r]$
	$x^~r[r(r-1)+7r+25]$
	as raízes são 
	$x = -3\pm4i$ 
	então a fómula será no formato
	$x^{-3+4i}$
	$C_1x^{-3}(\cos (4\ln x)+C_2x^{-3}i \sin (4\ln x))$
	
3. Raízes repetidas
	Quando a raiz têm multiplicidade, a solução será $\begin{cases} y_1=x^r \\ y_2 = x^r\ln (x)\end{cases}$
	Para o caso de segunda ordem
	$\displaystyle r= \frac{-(p_0-1)}{2}$ 
	_Exemplo_
	$9x^2y'' + 3xy'-8y=0$; com candidata 
	f(x) = $x^r$
	f' = $rx^{r-1}$
	f'' = $r(r-1)x^{r-2}$
	e obtemos: $9x^2r(r-1)x^{r-2}+3xrx^{r-1}-8x^r=0$
	fatoramos o $x^r$-> $x^r[9r(r-1)+3r-8]=0$
	resolvendo por báskara -> $\displaystyle r=\frac{6\pm18}{18}$