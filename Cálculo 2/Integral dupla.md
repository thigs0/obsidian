- Podemos calcular a integral dupla como o cálculo de duas [[Integral]]
Determine o volume do sólido $S$ delimitado pelo paraboloide elíptico $x^2+2y^2+z=16$ e os planos x=2,y=2 e os 3 planos coordenados

$R=[0,2]\times [0,2]$; $S=R\times \{ 0\leq z\leq 16-x^2-2y^2\}$
$V = \iint_R zdA =\iint_R (16-x^2-2y^2)dA = \int_0^2\int_0^2 16-x^2-2y^2dxdy= \int_0^2 [16x-\frac{x^3}{3}-2y^2x]|_0^2$ 
$=\int_0^2 88/3 -4y^2dy= (88/3)y -(4/3)y^3|_0^2$

**Exemplo**
D- Região limitada pelas parábolas $y=2x^2$; $y=1+x^2$
$\iint_D (x+2y)dA =?$
intersecção $2x^2=1+x^2$ => $x=\pm 1$, $y=2$
$D: x:-1\leq x\leq 1, y:2x^2\leq y\leq 1+y^2$

$$\iint (x+2y)dA=\int_{-1}^1\int_{2x^2}^{1+x^2}(2+2y)dydx$$


###### Em coordenadas polares
- Aproveitar a simetria circular
$$\iint_R f(x,y)dA=\int_{\alpha}^\beta\int_a^b f(r\cos \theta,r\sin \theta)rdrd\theta$$
**Exemplo**
$\iint_R(3x+4y^2)dA =\int_0^\pi \int_1^2 [3r\cos \theta +4r^2\sin^2\theta]rdrd\theta = \frac{15\pi}{2}$