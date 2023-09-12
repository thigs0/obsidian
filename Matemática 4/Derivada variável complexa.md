	$f'(z_0) = u_x(x_0,y_0)+iv_x(x_0,y_0)$

Propriedades 
- $D(f+g)(z) = Df(z) + Dg(z)$
- $D(f \cdot g)(z) = f(z).Dg(z)+g(z)Df(z)$
- Se $g(z) \neq 0$, então $\displaystyle D\frac{f}{g} = \frac{1}{g(z)^2}\left[ g(z)Df(z)-f(z)Dg(z)\right]$


**[[Limite]]** de uma função complexa
 Definição $\displaystyle \lim_{Z \to z_0} f(z) = W_0$ <==> $\forall \epsilon, \exists \delta >0$ tq $0 < |Z - Z_0|< \delta$ => $|f(z)-W_0| < \epsilon$
**Teorema**
Sejam $\displaystyle \lim_{z \to z_0} f(z) =w_0$ e $\displaystyle \lim_{z \to z_0} F(z) =W_0$
- $\displaystyle \lim_{z \to z_0}[f(z)+F(z)]= w_0 +W_0$  Limite da soma é a soma dos limites
- $\displaystyle \lim_{z \to z_0}[f(z).F(z)]= w_0 .W_0$     Limite do produto é o produto dos limites
- $\displaystyle \lim_{z \to z_0}[\frac{f(z)}{F(z)}]= \frac{w_0}{W_0}$ desde $W_0  \neq 0$ O limite da divisão é a divisão do limite

Como não faz sentido comparar tamanho entre dois [[Números complexos]], apenas seus módulos. Não faz sentido quando dizemos que Z-> $\large \infty$ 
Para isso, foi definida a **[[Esfera de Riemann]]**

**Teorema** [[Equações de Cauchy-Riemann]]
	Seja f(z) = u(x,y) + iv(x,y) e suponha que exista a derivada f'(z) em um ponto $z_0 = x_0+iy_0$. Então as derivadas parciais de primeira ordem de u e v existem em ($x_0,y_0$) e satisfazem as equações de Cauchy-Riemann
	Para obté-las, tomaremos dois caminhos para $\displaystyle f'(z_0) = \lim_{(\Delta x, \Delta y) \to (0,0)}\frac{(u(x+\Delta x , y+\Delta y) +iv(x +\delta x, y+\Delta y)) - (u(x,y) + iv(x,y))}{\Delta x + i\Delta y}$ 
	1) $\Delta x = 0$-> Andar sobre o eixo imaginário
		$f'(z_0)$
	$\displaystyle \large \begin{cases} u_x =v_y \\ u_y = -v_x\end{cases}$   <=> $\displaystyle \large \begin{cases} \frac{du}{dx}=\frac{dv}{dy}\\ \frac{du}{dy}= - \frac{dv}{dx}\end{cases}$
	São condições necessárias