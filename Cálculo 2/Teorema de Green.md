O teorema de Green fornece a relação entre uma [[Integral de linha]] ao redor de uma curva
fechada simples C e uma [[Integral]] dupla sobre a região do plano D delimitada por C. (Veja a
Figura 1. Assumimos que D é constituído por todos os pontos dentro de C, bem como todos
os pontos de C.) Ao enunciarmos o Teorema de Green, usamos a convenção de que a orientação positiva de uma curva fechada simples C refere-se ao sentido anti-horário de C, percorrido uma só vez. Assim, se C é dada pela função vetorial r(t), $a \leq t\leq b$, então a região
D está sempre do lado esquerdo quando r(t) percorre C. 

- ####### *Reduz uma integral de linha complicada para uma integral dupla*

- ### Hipóteses
--> Curva é fechada
--> Curva é orientada positivamente
--> O campo não pode ter singularidade
--> Precisa ser contínuo e suas [[Derivada]]s primeiras existam
$$\iint_C Pdx+Qdy =\iint_D\left( \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)dA$$

$$\int_c \vec F \cdot d\vec r = \iint_D\left( \frac{\partial F_x}{\partial x}-\frac{\partial F_y}{\partial y}\right)dxdy$$ ou
$$\iint_D Rot\vec F \cdot\vec kda = \int_{\delta D}\vec F d\vec r$$
Em que C é uma curva fechada e D é a região interna da curva fechada

**Exemplo**:
	Calcule $\int_C x^4dx+xydy$; onde C é a curva triangular constituída pelos segmentos de reta de (0, 0) a (1, 0), de (1, 0) a (0, 1), e de (0, 1) a (0, 0).
	![[fig1.png]]
	Temos:
	$\displaystyle \int_0^1 \int_0^{1-x}\frac{\partial xy}{dx}-\frac{\partial x^4}{dy}$ = $\displaystyle \int_0^1 \int_0^{1-x} (y-0)$ = $\displaystyle\int_0^1 \frac{(1-x)^2}{2}-\frac{0^2}{2}$ = $\displaystyle \int_0^1 1/2 -\frac{2x}{2}+\frac{x^2}{2}$ =  $\displaystyle \frac{1}{2}-\frac{x^2}{2} + \frac{x^3}{6}$ = 