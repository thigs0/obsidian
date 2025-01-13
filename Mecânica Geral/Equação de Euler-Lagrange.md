**Problema**: Extremize uma função da forma
$$I=\int_{x_a}^{x_b}dxf(x,y(x), y'(x))$$
A família de funções $\bar y(x, \epsilon)$ satisfaz
a) $\bar y(x_a,\epsilon))=y_x$, $\bar y(x_b),\epsilon)=y_b$
b) $\bar y(x,0)=y(x)$
c) $\bar y$ e suas [[Derivada]]s são contínuas até segunda ordem
$\frac{di}{d\epsilon}|_{\epsilon=0}=0$
$\displaystyle \frac{dI}{D\epsilon}=\int_{x_a}^{x^b}dx\left[\frac{\partial f}{\partial y}\frac{\partial \bar y}{\partial \epsilon}+\frac{\partial f}{\partial \bar y}\frac{\partial\bar y}{\partial \epsilon}\right]$ 
note que: 

![[function_plan.png|600]]

Neste caso $I(\epsilon)=\int_{x_a}^{x_b}dxf(x,\bar y,\bar y')$
com [[Condições de otimalidade]] $\displaystyle \frac{dI}{d\epsilon}|_{\epsilon=0}=0$
$\displaystyle \frac{dI}{d\epsilon}=\int_{x_a}^{x_b}dx\left[ \frac{\partial f}{\partial \bar y}\frac{\partial \bar y}{\partial \epsilon}+\frac{\partial f}{\partial \bar y'}\frac{\partial \bar y'}{\partial \epsilon} \right]$ usando o [[Teorema de Schwartz-Clairaut]]
$\displaystyle \frac{dI}{d\epsilon}=\int_{x_a}^{x_b}dx\left[ \frac{\partial f}{\partial \bar y}\frac{\partial \bar y}{\partial \epsilon}+\frac{\partial f}{\partial \bar y'}\frac{d}{dx}\left( \frac{\partial \bar y}{\partial \epsilon} \right) \right]$
$\displaystyle \frac{dI}{d\epsilon}=\int_{x_a}^{x_b}dx\frac{\partial f}{\partial \bar y}\frac{\partial \bar y}{\partial \epsilon}+\left[ \frac{\partial f}{\partial \bar y}\frac{\partial \bar y}{\partial \epsilon} \right]_{x_a}^{x_b}-\int_{x_a}^{x_b}dx\frac{d}{dx}\left(\frac{\partial f}{\partial \bar y'}\right)\frac{\partial \bar y}{\partial \epsilon}$
$\displaystyle \frac{\partial \bar y}{\partial \epsilon}|_{x=x_a}=\frac{\partial \bar y}{\partial \epsilon}|_{x=x_b}=0$ Posições fixas por definição do problema

$\displaystyle \left[\frac{dI}{d\epsilon}\right]_{\epsilon=0}=\int_{x_a}^{x_b}dx\left[ \frac{\partial f}{\partial \bar y}-\frac{d}{dx}\left( \frac{\partial f}{\partial \bar y} \right) \right]\left( \frac{\partial \bar y}{\partial \epsilon}_{\epsilon=0}\right)=0$

Como queremos analisar todas as soluções possíveis 
$$\frac{\partial \bar y}{\partial \epsilon} \neq 0 \Rightarrow \frac{\partial f}{\partial \bar y}-\frac{d}{dx}\frac{\partial f}{\partial \bar y}=0$$
Que é a equação de Euler-Lagrange

- Escrevendo uma outra versão sem dependencia de x
Considere $C=\frac{d}{dx}\left( y'\frac{\partial f}{\partial y'}-f \right)$
$\displaystyle c=y''\frac{\partial f}{\partial y'}+y'\frac{d}{dx}\frac{\partial f}{y'}-\frac{\partial f}{\partial x}-\frac{\partial f}{\partial y}y'-\frac{\partial f}{\partial y'}y''= y'\left[\frac{d}{dx}\frac{\partial f}{\partial y'}-\frac{\partial f}{\partial y} \right]-\frac{\partial f}{\partial x}$
Supomos que $\frac{\partial f}{\partial x}=0$ e o termo em colchetes é equivalente á equação de euler-lagrange. portanto
$$y'\frac{\partial f}{\partial y'}-f=constante$$
para n-[[Funções]]
$$\frac{\partial f}{\partial y_i}-\frac{d}{dx}\frac{\partial f}{\partial y'_i}=0,~~i=1,2,...,n$$


##### Exemplos
1) Menor trageto em um plano
$l=\int_\gamma ds=\int_\gamma dx\sqrt{1+y'^2}\Rightarrow f=\sqrt{1+y'^2}$ todo o caminho percorrido é dado por essa integral
$\displaystyle \frac{\partial f}{\partial y}-\frac{d}{dx}\frac{\partial f}{\partial y'}=0 \Rightarrow \frac{d}{dx}\frac{\partial f}{\partial y'}=0$ -> $\frac{\partial f}{\partial y'}=\frac{y'}{\sqrt{1+y'^2}}=constante$
=> $y'=\alpha constante$ => $y(x)=\alpha x+b$: [[Reta]]

2) Problema da [[Braquistocrona]]
Queremos encontrar o caminho que minimize o tempo entre dois pontos sobre ação da força gravitacional.
 elemento infinitesial de movimento é dado por
 $$dt=\frac{ds}{v}=\frac{\sqrt{dx^2+dy^2}}{v}=\frac{\sqrt{\left(dx/dy\right)^2+1}dy}{v}$$
 Pela conservação de energia potencial e cinética temos 
 $$v=\sqrt{2gy}$$
assim
$$dt=\frac{\sqrt{\left(dx/dy\right)^2+1}dy}{\sqrt{2gy}}\Rightarrow \Delta t=\frac{1}{\sqrt{2g}}\int_A^B\frac{\sqrt{{x'}^2+1}dy}{\sqrt{y}}$$
então nossa função f é $f=\frac{\sqrt{{x'}^2+1}dy}{\sqrt{y}}$

$\frac{\partial f}{\partial x}=0\Rightarrow y'\frac{\partial f}{\partial y'}-f=\frac{{y'}^2}{\sqrt{y(1+{y'}^2)}}=constante\Rightarrow \frac{1}{y(1+(y')^2)}=c$

é conveniente chamar $\frac{1}{C}=2a$
$y(1+{y'}^2)=2a\Rightarrow y'=\sqrt{\frac{2a-y}{y}}\Rightarrow dx=dy\sqrt{\frac{y}{2a-y}}$
usando a [[Integral]] de ambos os lados
$x-x_0=\int dy\sqrt{\frac{y}{2a-y}}$
$y=a(1-cos \theta)$, $dy=a\sin \theta d\theta$ 
$\displaystyle x-x_0=\int d\theta a\sin \theta \sqrt{\frac{a(1-cos \theta)}{a(1+cos \theta)}}=\int d\theta 2a \frac{\sin \theta}{2}\frac{\cos \theta}{2}\sqrt{\frac{\sin^2\frac{\theta}{2}}{\cos^2\frac{\theta}{2}}}=2a\int d\theta \sin^2 \frac{\theta}{2}=a(\theta -\sin \theta)$
Assim, a forma paramétrica da braquistrocrona é dada por 
$\begin{align}x=a(\theta -\sin \theta)+x_0 \\ y=a(1-\cos \theta) \end{align}$



###### Geodésica em plano
$l = \int_A^B ds=\int_\gamma \sqrt{dx^2+dy^2}=\int_{x_A}^{x^B}dx\sqrt{1+y'^2}$ 