1) Circulo com origem deslocada
![[circ.png|400]]
Usamos a fórmula da [[Circunferência]]
então $y=\pm \sqrt{R^2-x^2}$

2) Podemos considerar a fórma em [[coordenada Polar]]
$\begin{cases} x=R\cos(\theta) \\ y=R\sin(\theta)\end{cases}$ 


Abaixo temos o código em C++ que calcula a circuferência no primeiro quadrante e replica ele para o restante

3) Ponto médio: Consideramos a equação do item 1 modificada para dar um contexto de positivo ou negativo$$x^2+y^2-r^2=0$$
Como queremos um algoritmo incremental, temos o próximo ponto como $d_{old}=f(x_p+1, y_p-\frac{1}{2})$ e aplicamos na equação da circuferência 
$d_{neq}=F(x_p+2,y_p-\frac{1}{2})$ e aplicamos na equação da circuferência
e quando subtraimos uma equação da outra, obtemos
$$\begin{cases} \Delta_e= 2x_p+3\\ \Delta_{se}= 2x_p-2y_p+5 \end{cases}$$


4) 