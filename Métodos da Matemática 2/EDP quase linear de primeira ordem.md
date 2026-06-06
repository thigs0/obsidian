A forma geral de uma [[EDP]] quase linear de primeira ordem com n variáveis independentes é
$$\sum\limits_{i=1}^n A_i(u,x_1,...,x_n)u_{x_i}=G(u,x_1,...,x_n)$$
### Duas variáveis independentes
Vamos considerar apenas duas variáveis para permitir a interpretação geométrica. Denotando as variáveis independentes por x e y, escrevemos essa forma mais geral como
$$a(x,y,u)u_x+b(x,y,u)u_y=c(x,y,u)$$
Seja $u=u(x,y)$ uma solução dessa [[EDP]]. A função $\phi(x,y,u)=u-u(x,y)=0$  representa uma superfície no espaço de coordenadas $(x,y,u)$ denominada [[Superfície Integral]]. Uma vez que
$$0 = u_xdx+u_ydy-du=(u_x,u_y,-1)\cdot (dx,dy,du)$$
sabemos que o [[Vetor Normal]] a essa superfície integral é proporcional ao [[Vetor]] $(u_x,u_y,-1)$ no ponto $P=(x,y,u)$. Por outro lado, a equação pode ser vista
$$(a,b,c)\cdot (u_x,u_y,-1)=0$$
de onde podemos concluir que o vetor $(a,b,c)$ pertence ao plano tangente à superfície no ponto P. Esse vetor é o vetor tangente a uma curva, que iremos parametrizar por t, ou seja $(x,y,u)=(x(t),y(t),u(t))$. Devemos ter, portanto que
$$\begin{cases}\frac{dx}{dt}=a(x(t),y(t),u(t))\\ \frac{dy}{dt}=b(x(t),y(t),u(t))\\ \frac{du}{dt}=c(x(t),y(t),u(t))\end{cases}$$
Este é o [[Sistema de equações características]], ou simplesmente [[Sistema característico]]. Para determinar uma dessas curvas iniciais são dadas ao longo de uma curva inicial $\Gamma(s)=(x_0(s),y_0(s),u_0(s))$. Escolhendo o parâmetro t, de modo que a característica está localizada em $\Gamma(s)$ para $t=0$, temos
$$\begin{cases}x(0,s)=x_0(s)\\ y(0,s)=y_0(s)\\ u(0,s)=u_0(s)\end{cases}$$
Por outro lado, as derivadas em t são autônomo (não depende de t) e portanto, pode ser escrito na seguinte forma:
$$\frac{dx}{a}=\frac{dy}{b}=\frac{du}{c}$$
e podemos representar de outra maneira, que seja conveniente no problema
$$\frac{dy}{dx}=\frac{b}{a},~~ \frac{du}{dx}=\frac{c}{a}$$
#### Exemplo 1
Encontre a solução da EDP $$xu_x+yu_y=u$$
Avaliando o sistema característico
$$\frac{dx}{dt}=x,~~\frac{dy}{dt}=y,~~\frac{du}{dt}=u$$
Podemos encontrar as soluções de maneira 
$$x=c_1e^t,~~y=c_2e^t,~~~~u=c_3e^t$$

