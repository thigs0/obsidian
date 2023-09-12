Podemos reduzir uma [[Equação de Euler-Cauchy]] para uma [[Equação Diferencial linear de coeficiente constante]], que é mais fácil de se resolver
	_Exemplo_: Resolve a EDO $x^3y'''+6x^2y''+7xy'+y=0$
	$\begin{cases} y = x^r \\ y' = rx^{r-1}\\ y'' = r(r-1)x^{r-2}\\ y''' = r(r-1)(r-2)x^{r-3} \end{cases}$ --> Candidata a solução
	_
	Aplicando a candidata a solução dentro da equação
	$x^3r(r-1)(r-2)x^{r-3}+ 6 x^2r(r-1)x^{r-2}+7xrx^{r-1}+x^r=0$
	$x^r[r(r-1)(r-2)+ 6r(r-1)+7r+1]=0$
	e encontramos as raízes
	.
	.
	definimos a função y de forma Y(t(x)) e $x=e^t \Rightarrow t(x) = \ln (x)$ encontramos as suas derivadas
	$\displaystyle \large \begin{cases} \frac{dy}{dt}= \frac{dy}{dt}\frac{dt}{dx}= \frac{dy}{dt} \frac{1}{x}\\ \frac{dx}{dx}[\frac{dy}{dx}]= \frac{dy}{dx}[\frac{dy}{dt}\frac{1}{x}]= \frac{1}{x^2}[\frac{d^2y}{dt^2}-\frac{dy}{dt}]\\\frac{d^3y}{dx^3}=\frac{1}{x^3}[\frac{d^3y}{dt^3}-\frac{d^2y}{dt^2}]\end{cases}$--> Substituimos as deriavdas na equação

## **Equações não homogêneas via o método de coeficientes indeterminados**
_Exemplos_
	$y''-y''-2y = 3x+4$ 
	1. Observamos o formato da f(x) e supomos uma solução no mesmo formato
	 $Y_p = Ax+B$
	 $\begin{cases} y_p = ax+b \\y_p' = a\\ y_p''=0\end{cases}$
	 $0+a-2(ax+b)=3x+4 = a-2ax+b$
	 Resolvemos o sistema $\begin{matrix} \end{matrix}$

**Teorema**:
	Se $y_1$ e $y_2$ forem duas soluções da equação não homogênea, então sua diferença $y_1 - y_2$ é uma solução da equação homogênea associada. Se, além disso $y_1$ e $y_2$ formarem um conjunto fundamental de soluções para a equação, então 	
	$y_1 - y_2 = c_1 y_1 +c_2y_2$, em que $c_1$ e $c_2$ são constantes determinadas

- **[[Variação dos parâmetros]]** ou [[Método de Lagrange]]
	resolve [[EDO]] não homogênea, é um método geral 
	_Exemplo_:
		$y''+4y=8 \tan t;~~~ -\pi /2 <t <\pi /2$