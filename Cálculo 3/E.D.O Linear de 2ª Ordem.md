
- **Definição**
	D é o operador de derivaçãod e f e (D-3)y, derivavamos e multiplicamos o resultado por -3;
	vantagem de drescerver a equação característica


**_Teorema_**
	Suponha que as funções $M,N,M_x~e~N_x$ em que os índices denota m derivadas parciais, são contínuas em uma região retangular R: $\displaystyle \alpha < x< \beta,~\gamma <y<\delta$.Então temos a equação$$M(x,y)+N(x,y)y'=0$$
	Será uma equação diferencial exata em R se, e somente se,$$M_y(x,y)+N(x,y)y'=0$$
	Em cada ponto de R.Ou seja, existe uma função $\psi$ satisfazendo as equações acima$$\psi_x(x,y)= M(x,y)~,~ \psi_y(x,y)=N(x,y)$$

Equação linear de ordem n

$$P_n(x)y^{(n)}+ P_{n-1}(x)y^{(n-1)}...P_{1}y^{(1)}+P_{0}y=F(x)$$

- Se F(x) = 0, a [[EDO]] é homogênea

Podemos facilitar e dividir os índices por $P_n(x)$ e obtemos
$P_{n-1}(x)y^{(n-1)}...P_{1}y^{(1)}+P_{0}y=F(x)$

[[Existência e unicidade]]
 1. Dado que $P_i(x)$ são coeficientes contínuos em I aberto
 2. f(x) contínua

- Dada uma equação no formato

$$M(x,y)dx + N(x,y)dy =C$$

Se $M_y = N_x$, então a equação é exata e existe F(x,y) = C com

$$\begin{cases} F_x = M \\ F_y = N \end{cases}$$

assim, podemos integrar $F_x = M$ e obtemos $F(x,y)= \int \left[M(x)dx \right] + G(x)$; de modo que G(y) para este caso é uma constante

e usamos o segundo caso para encontrar a constante $G(y)$

-Se $M_y \neq N_x$
	A equação é não exata,, mas podemos multiplicar por um fator u(x,y) que torne a equação exata
	de modo a obter: $u(x,y).M(x,y)dx + u(x,y)N(x,y)dy =C$ de forma exata
	
	$\displaystyle \frac{d[uM]}{dy} = \frac{d[uN]}{dx}$
	_Supomos que u(x,y)=u(y)_ depende apenas de y
	e obtemos $\displaystyle \frac{d[uM]}{dy} = \frac{d[uN]}{dx}\Rightarrow u’(y)M +M_yu(y) = 0.N+u(y)N_x \Rightarrow u’(y)M = (N_x-M_y)u(y) \Rightarrow \int \frac{u’}{u}dy= \int\frac{N_x-M_y}{M}dy$
	Se $\displaystyle \frac{N_x-M_y}{M}$ é função apenas de y, podemos integrar em relação a dy
	e temos $\displaystyle u(y) = e^{ \int\frac{N_x-M_y}{M}dy}$

#### Equações características
**Equações difenciais homogêneas de coeficientes constantes**:
são dadas na forma $y''+p(t)y'+q(t)y=g(t)$
	A solução sempre será da forma $\large e^{rt}$
	Assim temos os seguintes sistemas
	$\large \begin{cases} y_1 = e^{rt}\\ y_1' = re^{rt}\\ y_1'' = r^2e^{rt}\\..\\ y_1^{(n)}= r^ne^{rt}\end{cases}$ e com este sistema, substituimos na equação
	e encontramos a equação característica no formato $(ar^2+br+c)e^{rt}=0$, como $\large e^{rt}$ não é 0. resolvemos a equação ao lado

é necessário um sistema [[Linear dependente]]
_**Teorema**_:
	Se $f_1,f_2,...f_n$ são [[Linear dependente]] $\Rightarrow$ [[Wronskiano]] ($W(f_1,f_2,...f_n)$) = 0
	$$W(f_1,f_2,f_3,...,f_n)= \begin{vmatrix} f_1& f_2 & f_3&...&f_{n-1}&f_n\\ f_1^{(1)}& f_2^{(1)} & f_3^{(1)}&...&f_{n-1}^{(1)}&f_n^{(1)}\\ ...&...&...&...&...&...\\ f_1^{(n-1)}& f_2^{(n-1)} & f_3^{(n-1)}&...&f_{n-1}^{(n-1)}&f_n^{(n-1)}\end{vmatrix}=0$$
	_Para soluções_
	$Ly=0$ sejam$(y_1,y_2,y_3,...y_n)$ soluções I <- [[Existência e unicidade]] 
	a) Se $y_1,y_2,y_3,...y_n$ são linearmente dependentes temos $W(y_1,y_2,y_3,...y_n) =0$ para todo $x \in I$
	b) Se $(y_1,y_2,y_3,...y_n)$ são [[linear indepenpende]] então $W(y_1,y_2,y_3,...y_n) \neq 0$

[[Teorema de Abel]]
	Se $y_1$ e $y_2$ forem soluções da equação diferencial  $L(y) = y'' +p(t)y'+q(t)y=0$ em que p e q são contínuas em um intervalo aberto i, então o [[Wronskiano]] será dado por $$W(y_1,y_2)=ce^{-\int p(t)dt}$$
	Prova:
	Temos duas soluções para a edo
	$\begin{cases} y_1''+py_1'+qy_1=0\\ y_2''+py_2'+qy_2=0\end{cases}$
	Se multiplicarmos a linha 1 por $-y_2$ e a linha 2 por $y_1$ e somarmos. Obtemos:
	$(y_1y_2''-y_1''y_2)+p(y_1y_2'-y_1'y_2)=0$
	e este é a derivada do [[Wronskiano]], então
	$W'+pW=0$, resolvendo encontramos a equação de Abel