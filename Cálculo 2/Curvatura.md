A curvatura de C em um dado ponto é a medida de quão rapidamente a curva muda de direção no ponto. Especificamente, definimos a curvatura como o módulo da taxa de variação do [[Vetor]] tangente unitário com relação ao comprimento do arco
$$k = \left|\frac{dT}{ds}\right|\rightarrow \frac{dT/dt}{\underbrace{ds/dt}_{|r'(t)|}}=\left| \frac{T'(t)}{r'(t)}\right|$$

#### Teorema
A curvatura de uma curva dada pela [[Função vetorial]] r é:
$$k(t) = \frac{|r'(t)\times r''(t)|}{|r'(t)|^3}$$
**Demonstração**
$r'(t) = T.|r'|$
$r''(t)\left(\frac{d(T.|r'|)}{dt}\right)^2(T\times T')= \left( \frac{ds}{dt}\right)^2.\left( \frac{r'}{|r'|}\times \frac{r''}{|r''|}\right)$
Temos $|T(t)|=1$; $T\times T'=|T|.|T'|sen(\pi/2)$ => $|r'\times r''|=\left(\frac{ds}{dt}\right)^2|T\times T'|)= \left(\frac{ds}{dt}\right)^2|T'|$
=> $\displaystyle |T'|=\frac{|r'\times r''|}{(ds/dt)^2}=\frac{|r'\times r''|}{|r'|^2}$ 
por fim
$$k=\frac{|T'|}{|r'|}=\frac{|r'\times r''|}{|r'|^3}$$
**Exemplo**
$r(t) = (t, t^2,t^3)$ em (0,0,0)
$r'(t)=(1,2t,3t^2)$
$r''(t)=(0,2,6t)$
$|r'(t)|=\sqrt{1+4t^2+9t^4}$

$\displaystyle r'(t)\times r''(t)=\begin{vmatrix}i & j & k \\  & 1 & 2t & 3t^2 \\ 0 & 2 & 6t\end{vmatrix}=6t^2\hat i-6t\hat j+2\hat k$
$|r'(t)\times r''(t)|=\sqrt{36t^4+36t^2+4}=2\sqrt{9t^4+9t^2+1}$
$\displaystyle k = \frac{|r'\times r''|}{|r'|^3}=\frac{2\sqrt{9t^4+9t^2+1}}{(1+4t^2+9t^4)^{3/2}}$
com t=0 => k(0) = 2 

