Seja f uma função analítica, temos que a integral fechada sobre uma curva é 0$$\oint_c f(z)dz =0$$
Prova:
	Seja c uma curva qualquer no plano e que tenha uma parametrização f(g(t)), $t \in [0, 2\pi]$ e seja orientada positivamente
	![[curva_fechada.png]]
	Temos $\displaystyle \oint_c f(z)dz = \oint_c f(z(t)z'(t)dt$
	pela representação em u(t)+iv(t), obtemos
	$f(z(t))\cdot z'(t) = [u(x(t), y(t))+iv(x(t), y(t))](x'(t) +iy'(t))$
	Ao multiplicarmos e juntarmos a parte real e imaginária, obtemos
	$[u(x(t), y(t))x'(t)-v(x(t), y(t))y'] +i[v(x(t), y(t))x'(t) +u(x(t), y(t))y'(t)]$ 
	= $(ux'-vy')+i(vx'+uy')$
	Então $\displaystyle \oint_c f(z(t))z'(t)dt = \oint_c ux'-vy' dt +i\oint_c vx'+uy'$
	Que pode ser visto como a [[Derivada Parcial]] em termos de x e y =>
	$\displaystyle \oint_c (u_x - v_y)dt +i\oint_{c} (v_x+u_y)$ usando as [[Equações de Cauchy-Riemann]] obtemos que é 0 ambas as integrais

**Exemplo**

---

Para um Domínio multi-conectado

Dado uma curva C que tem pontos singulares internos que podem ser representados por uma pequena circunferência

$$\large \oint_c f(z)dz - \sum_{k=1}^n \oint_{C_k} f(z)dz =0$$
