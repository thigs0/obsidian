Supomos que a função f é limitada superiormente e é [[Função analítica]] em em alguma vizinhança removendo $0<|z-z_0|<\epsilon$ de $z_0$ ,Se e somente se tem uma [[Singularidade removível]].
	Prova:
	Como a função não é analítica em $z_0$, temos a seguinte [[Série de Leurent]]
	$$f(z)=\sum_{n=0}^\infty a_n(z-z_0)^n+\sum_{n=1}^\infty \frac{b_n}{(z-z_0)^n}$$
	E sabemos que o coeficiente $b_n$ tem forma
	$$b_n=\frac{1}{2\pi i}\int_c \frac{f(z)dz}{(z-z_0)^{-n+1}}\hspace{1cm}n=1,2,3,4$$
	Sendo c uma [[Circunferência]] de raio $\rho$ como na figura abaixo
	![[curva_teorema_riemann.png|center|450]]
	Como temos que f é limitada tal que $|f(z)|\leq m$ => $\displaystyle \left|\int_{c}f(z)dz\right| \leq M C$ 
	Com a informação acima, analisamo que 
	$\displaystyle |b_n| = \left| \frac{1}{2\pi i}\int_c \frac{f(z)dz}{(z-z_0)^{-n+1}}\right| \leq \left| \frac{1}{2\pi i}\right|\left| \int_c \frac{f(z)dz}{(z-z_0)^{-n+1}}\right| = \frac{1}{2\pi}\frac{1}{\rho^{-n+1}} \int_{c} f(z)dz$ 
	como a integral também está limitada, temos
	$$\frac{1}{2\pi}\frac{1}{\rho^{-n+1}}M.2\pi\rho = M.\rho^n$$
	Assim, basta tomar o [[Limite]] de $\displaystyle \lim_{\rho \to 0} M\rho^n$ e obtemos que $|b_n|\leq 0$. Então $b_n$ é 0 e a singularidade é removível
	(<-) Provando a volta
	Se a singularidade é removível, existe uma expressão em série de potência
	$\displaystyle f(z)=\sum_{n=0}^{\infty}a_nz^n$, assim, $\displaystyle \int_c f(z)=\sum_{n=0}^\infty \int_c a_nz^n$ = $\displaystyle \sum_{n=0}^{\infty} a_n\frac{z^n+1}{n+1}=\sum_{n=0}^\infty b_n(z^n+1)$ Como temos uma nova [[Séries de Potências]], então para um ponto $z_0$ a série é limitada por $M \in \mathbb{R}$ 
	 