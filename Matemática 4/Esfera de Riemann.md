Como uma esfera com o pelo sul tocando o plano complexo na origem
![[Esfera_riemann.png]]
Iniciando no polo norte, temos um ponto da esfera e com isso obtemos qualquer ponto no plano

Para calcularmos. O ponto da esfera é (X,Y,Z) e o ponto do plano é (x,y,z)

Quando Y=0 => y=0 e podemos simplificar a representação 
![[geometria.png]]
Temos um triângulo retângulo com o eixo z e o ponto da esfera e um triangulo retangulo do mesmo eixo e o ponto no plano. Pela semelhança de triângulos
$\displaystyle \frac{2-Z}{X}=\frac{2}{x}$=> $\displaystyle x = \frac{2X}{2-Z}$ 
e o quando X=0 => x=0
$\displaystyle \frac{2-Z}{Y} = \frac{2}{y}$ => $\displaystyle y = \frac{2Y}{2-Z}$ 
e pela equação da esfera
$\displaystyle X^2 +Y^2+(Z-1)^2=1$

Obtemos por fim os pontos da esfera de riemann
$\displaystyle X = \frac{4x}{x^2+y^2+4}$,    $Y = \displaystyle \frac{4y}{x^2+y^2+4}$ , $Z = \displaystyle \frac{2(x^2+y^2)}{x^2+y^2+4}$

*Quando tomamos o limite de x e y* -> $\infty$ 
e temos que (X,Y,Z) -> (0,0,2)


**Exemplo**
Calcule $\displaystyle \large \lim_{z \to \infty} \frac{1}{z}$ = u+iv
Achamos o valor de u e v
$\displaystyle \frac{1}{z} = \frac{1}{x+iy}=\frac{1}{x+iy}.\frac{x-iy}{x-iy}= \frac{x-iy}{x^2+y^2}$=> $\displaystyle u=\frac{x}{x^2+y^2}$ e $\displaystyle y = \frac{-y}{x^2+y^2}$

Agora passamos u e v para a esfera de riemann da imagem


