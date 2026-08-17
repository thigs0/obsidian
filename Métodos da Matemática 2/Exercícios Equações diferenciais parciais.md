Livro métodos matemáticos Volume 2 - Jayme Vaz Jr

2. 
 a)
 $$\begin{cases}u_y+cu_x=0\\u(y,y)=\sin(y)\end{cases}$$
Sabemos que $\begin{cases}a=c\\b=1\\c=0\end{cases}$, agora considerando cada componente em relação a variável t
$\displaystyle \begin{cases}\frac{dx}{dt}=c\Rightarrow dx=cdt\Rightarrow x=ct+f_1(s)\\ \frac{dy}{dt}=1\Rightarrow dy=dt\Rightarrow y=t+f_2(s) \\ \frac{du}{dt}=0\Rightarrow du=0dt\Rightarrow u=f_3(s) \end{cases}$, encontrando agora as contentes de integração que dependem apenas de s
Aplicando as condições iniciais $\begin{cases}u(0,s) = \sin(s) = f_3(s)\\ y(0,s)=f_2(s)=s\\ x(0,s)=f_1(s)=s\end{cases}\Rightarrow \begin{cases}x=ct+s\\ y=t+s\\u=\sin(s)\end{cases}$ 
isolamos t na equação dois ($y-s=t$) e aplicamos na primeira $\displaystyle s=\frac{x-cy}{1-c}$ e por fim aplicamos na terceira

$$\boxed{u(x,y)=\sin\left(\frac{x-cy}{1-c}\right)}$$
b)
$$\begin{cases}u_y+uu_x=0\\u(x,0)=f(x)\end{cases}$$
Sabemos que $\begin{cases}a=u\\b=1\\c=0\end{cases}$, então encontraremos as componentes de t
$\begin{cases} \frac{dx}{dt}=u\Rightarrow dx=udt\Rightarrow x=ut+f_1(s)\\ \frac{dy}{dt}=1\Rightarrow dy=d\Rightarrow y=t+f_2(s)\\ \frac{du}{dt}=0\Rightarrow du=0dt\Rightarrow u=f_2(s) \end{cases}$, aplicamos as condições iniciais para encontrar as constantes dependentes de s
$$\begin{cases} u(s,0)=f_3(s)=f(s)\\ y(s,0)=0+f_2(s)=0\\ x(s,0)=f_1(s)=s \end{cases}\Rightarrow \begin{cases}u(s,t)=f(s)\\y(s,t)=t\\ x(s,t)=tf(s)+s\end{cases}$$
Para retornar para as coordenadas $(x,y)$, pela terceira equação aplicando que $y=t$ => $x-yu=s$. Aplicamos na primeira equação $$\boxed{u(x,y)=f(x-uy)}$$
c)
$$\begin{cases}2u_x-u_y=0\\ u(x,0)=\sin(x)\end{cases}$$
Sabemos que $\begin{cases}a=2\\b=-1\\c=0\end{cases}$, agora consideramos em relação a t
$\begin{cases}\frac{du}{dt}=0\Rightarrow du=0dt\Rightarrow u=f_1(s)\\ \frac{dy}{dt}=-1\Rightarrow dy=-dt\Rightarrow y=-t+f_2(s)\\ \frac{dx}{dt}=2\Rightarrow dx=2dt\Rightarrow x=2t+f_3(s)\end{cases}$, aplicamos as condições iniciais para encontrar as constantes dependentes de s
$$\begin{cases}x(0,s)=s=f_3(s)\\y(0,s)=0=f_2(s)\\u(0,s)=sen(s)=f_1(s)\end{cases}\Rightarrow \begin{cases} x(s,t)=2t+s \\y(s,t)=-t\\u(s,t)=\sin(s)\end{cases}$$

Sendo que $y=-t$, aplicamos na primeira formula e isolamos o s para obter $x+2y=s$. Por fim aplicamos na terceira
$$\boxed{u(x,y)=\sin(x+2y)}$$
d)
$$\begin{cases}2u_x+uu_y=0\\ u(x,0)=f(x)\end{cases}$$
Sabemos que $\begin{cases}a=2\\b=u\\c=0\end{cases}$, agora considerando em relação a $t$
$\begin{cases}\frac{du}{dt}=0\Rightarrow u=f_1(s)\\ \frac{dy}{dt}=u\Rightarrow \frac{dy}{dt}=f_1(s)\Rightarrow y=f_1(s)t+f_2(s)\\ \frac{dx}{dt}=2\Rightarrow dx=2dt\Rightarrow x=2t+f_3(s)\end{cases}$, considerando agora a condição inicial
$$\begin{cases}x(s,0)=f_3(s)=s\\ y(s,0)=0f_1(s)+f_2(s)=f_2(s)=0\\ u(s,0)=f_1(s)=f(s)\end{cases}\Rightarrow \begin{cases} x(s,t)=2t+s\\y(s,t)=f(s)t\\u(s,t)=f(s) \end{cases}$$
Pela equação dois encontramos ($t=\frac{y}{u}$) na primeira e isolamos ($s=x-\frac{2y}{u}$) e aplicamos na terceira
$$\boxed{u=f\left(x-\frac{2y}{u}\right)}$$
e)
$$\begin{cases} xu_x+yu_y=x\\ u(x,x^2)=e^{-x} \end{cases}$$
Sabemos que $\begin{cases}a=x\\b=y\\c=x\end{cases}$, agora considerando sobre a variável t
$\begin{cases} \frac{dx}{dt}=x\Rightarrow \frac{dx}{x}=dt\Rightarrow x=e^{t+f_1(s)}\\ \frac{dy}{dt}=y\Rightarrow \frac{dy}{y}=dt\Rightarrow y=e^{t+f_2(s)}\\ \frac{du}{dt}=x\Rightarrow du=e^tsdt\Rightarrow u=se^t+f_3(s) \end{cases}$,considerando agora a condição inicial
$$\begin{cases}x(s,0)=e^{f_1(s)}=s\Rightarrow f_1(s)=\ln(s)\\y(s,0)=e^{f_2(s)}=s^2\Rightarrow f_2(s)=\ln(s^2)\\ u(s,0)=e^{-x}=e^{-s}\Rightarrow f_3(s)=e^{-s}-s\end{cases}\Rightarrow \begin{cases} x(s,t)=e^ts\\ y(s,t)=e^ts^2\\ u(s,t)=se^t+e^{-s}-s \end{cases}$$
Dividindo a segunda equação pela primeira, obtemos $\displaystyle s=\frac{y}{x}$. Usamos as relações para na terceira obter
$$\boxed{u(x,y)=x+e^{-y/x}-\frac{y}{x}}$$
f)
$$\begin{cases}u_y+u_x=u\\ u(0,y)=\displaystyle \frac{1}{1+y^2}\end{cases}$$
Sabemos que $\begin{cases}a=1\\b=1\\c=u\end{cases}$, com isso encontramos as funções em t
$\begin{cases} \frac{dx}{dt}=1\Rightarrow dx=dt\Rightarrow x=t+f_1(s)\\ \frac{dy}{dt}=1\Rightarrow y=t+f_2(s)\\ \frac{du}{dt}=u\Rightarrow \frac{du}{u}=dt\Rightarrow u=e^{t+f_2(s)} \end{cases}$, Agora consideramos as condições iniciais para encontrar as funções de f
$$\begin{cases} x(s,0)=f_1(s)=0\\ y(s,0)=f_2(s)=s\\ u(s,0)=\frac{1}{1+s^2}\Rightarrow f_2(s)=\ln(1)-\ln(1+s^2) \end{cases}\Rightarrow \begin{cases}x=t\\y=t+s\\u=\displaystyle \frac{e^t}{1+s^2}\end{cases}$$
Aplicamos a primeira equação na segunda e isolamos, obtendo $s=y-x$. Para aplicar na terceira
$$\boxed{u(x,y)=\frac{e^x}{1+(y-x)^2}}$$
g)
$$\begin{cases}(y+u)u_x+(u+x)u_y=x-y\\ u(x,0)=1+x\end{cases}$$
h)
$$\begin{cases} u_x+uu_y=1\\ u(0,y)=y\end{cases}$$
Sabemos que $\begin{cases} a=1\\b=u\\c=1 \end{cases}$, Agora considerando as condições iniciais para encontrar as funções de s
$\begin{cases} \frac{dx}{dt}=1\Rightarrow dx=dt\Rightarrow x=t+f_{1(s)} \\ \frac{du}{dt}=1\Rightarrow du=dt\Rightarrow u=t+f_3(s) \\ \frac{dy}{dt}=u=t+f_3(s)\Rightarrow u=\frac{x^2}{2}+tf_3(s)+f_2(s) \end{cases}$, agora considerando as condições iniciais
$$
\begin{cases} x(0,s)=f_1(s)=0\\y(0,s)=f_2(s)=s\\ u(0,s)=s=f_3(s) \end{cases}\Rightarrow \begin{cases} x=t\\ y=\frac{t^2}{2}+ts+s\\ u=s+t \end{cases}
$$
Aplicamos a primeira equação na terceira para obter, $u-x=s$. E aplicamos na segunda, isolando o u
$$\boxed{u=\frac{y+\frac{x^2}{2}+x}{x+1}}$$

i)
$$\begin{cases}uu_x-uu_y=xy,x\geq 0,y\geq 0\\ u(0,y)=e^{-y^2}\\ u(x,0)=e^{-x^2}\end{cases}$$
Sabemos que $\begin{cases} a=u\\b=-u\\c=xy \end{cases}$, agora tomando em relação a variável t
$$\begin{cases} \begin{align} \frac{dx}{dt}=u\\ \frac{dy}{dt}=-u\end{align}\Rightarrow \frac{dy}{dt}+\frac{dx}{dt}=u-u=0\Rightarrow \frac{d(y+x)}{dt}=0\Rightarrow y+x=f_1(s) \\ \frac{du}{dt} =xy=x(f_1(a)-x) \end{cases}$$
Como deixamos a terceira equação em função de x, usamos outra propriedade que permite integrar nas variáveis separadas $\frac{du}{dx}=\frac{f_1(s)-x}{u}\Rightarrow \frac{u^2}{2}=\frac{x^2}{2}f_1(s)-\frac{x^3}{3}+f_2(s)$.

Neste caso temos duas condições, considerando a primeira ( $u(0,y)=e^{-y^2}$ )
$\begin{cases}x(s,0)=0\\ y(s,0)=y=s\\ u(s,0)=e^{-y^2}=e^{-s^2}=f_2(s)\end{cases};\hspace{6pt} y(s,0)+x(s,0)=0+s=f_1(s)~~\text{como é constante}\Rightarrow y+x=s$  

Substituindo as constantes e valores de s em $u^2/2$, encontramos
$$\frac{u^2}{2}=\frac{x^2(x+y)}{2}-\frac{x^3}{3}+\frac{e^{-2(y+x)^2}}{2}$$
$$u^2=x^2y+\frac{x^3}{3}+e^{-2(y+x)^2}$$

Considerando a segunda condição ($u(x,0)=e^{-x^2}$) 
$$\begin{cases}x(s,0)=x=s\\ y(s,0)=0\\ u(s,0)=e^{-x^2}=e^{-s^2}=f_2(s)\end{cases};\hspace{6pt} y(s,0)+x(s,0)=0+s=f_2(s)~~\text{como é constante}\Rightarrow y+x=s$$
Substituindo as constantes e valores de s em $u^2/2$, encontramos
$$\begin{align}\frac{u^2}{2}=\frac{x^2}{2}(x)+\frac{x^2}{2}(y)-\frac{x^3}{3}-\frac{e^{-2(x+y)^2}}{2}-\frac{(x+y)^3}{2}+\frac{(x+y)^3}{3}\\ 3u^2 = 3e^{-2(x+y)^2} - 3xy^2 - y^3\end{align}$$

Assim as duas equações juntas são

$$u(x, y) = \begin{cases} \sqrt{e^{-2(x+y)^2} + x^2y + \frac{x^3}{3}}, & y \geq x \\ \sqrt{e^{-2(x+y)^2} - xy^2 - \frac{y^3}{3}}, & x > y \end{cases}$$
j)
$$\begin{cases} x^2u_x-y^2u_y=0\\ u\to e^x~para~y\to \infty \end{cases}$$
Sabemos que $\begin{cases} a=x^2\\ b=-y^2\\c=0 \end{cases}$, considerando em relação a variável t
$\begin{cases}\frac{du}{dt}=0\Rightarrow du=0dt\Rightarrow u=f_1(s)\\ \frac{dx}{dt}=x^2\Rightarrow \frac{dx}{x^2}=dt\Rightarrow \frac{x^{-1}}{-1}=t+f_2(s)\Rightarrow x=\frac{-1}{t+f_2(s)}\\ \frac{dy}{dt}=-y^2\Rightarrow \frac{dy}{y^2}=-dt\Rightarrow \frac{y^{-1}}{-1}=-t+f_3(s)\Rightarrow y=\frac{1}{t+f_3(s)}  \end{cases}$
Aplicando a condição inicial, obtemos o valor das contantes
$$\begin{cases} x(s,0)=s \Rightarrow s=\frac{-1}{f_2(s)}\Rightarrow f_2(s)=\frac{-1}{s} \\ \begin{align}y(s,0)=0\\ \lim_{s\to \infty} u(s,0)=e^s\end{align}\Rightarrow \frac{1}{f_3(s)}=0\Rightarrow f_3(s)=\frac{1}{y} \end{cases}$$
$y=\frac{1}{(ty+1)/y}\Rightarrow ty+1=1\Rightarrow t=\frac{1}{y}$
Aplicamos t na equação de x
$x=\frac{-1}{\frac{1}{y}-\frac{1}{s}}\Rightarrow \frac{1}{y}-\frac{1}{s}=-\frac{1}{x}\Rightarrow \frac{1}{s}=\frac{1}{x}+\frac{1}{y}=\frac{y+x}{xy}\Rightarrow s=\frac{xy}{y+x}$
Aplicamos s na equação de u para obter
$$\boxed{u(x,y)=e^{\displaystyle\frac{xy}{x+y}}}$$
k)
$$\begin{cases} yu_x+xu_y=xy,x\geq0,y\geq0\\ u(0,y)=e^{-y^2}\\ u(x,0)=e^{-x^2} \end{cases}$$
Sabemos que $\begin{cases} a=y\\b=x\\u=xy \end{cases}$, observamos que as componentes $u_x$ depende de y e $u_y$ depende de x. Então usamos a relação entre essas duas variáveis.
$\frac{dy}{dx}=\frac{x}{y}\Rightarrow ydy=xdx\Rightarrow y^2-x^2=f_1(s)$
Como as condições são mistas, aplicamos as condições para reduzir a complexidade.
Aplicando a primeira condição
$$\begin{cases} x(s,0)=0\\ y(s,0)=y=s\\ u(s,0)=e^{-y^2}=e^{-s^2} \end{cases}\Rightarrow \frac{du}{dx}=\frac{xy}{y}=x\Rightarrow du=xdx\Rightarrow u=\frac{x^2}{2}+f_2(s)\Rightarrow f_2(s)=e^{-s^2}$$
$$\boxed{u=\frac{x^2}{2}+e^{-(y^2-x^2)}}$$
Aplicando a segunda condição
$$\begin{cases} x(s,0=x=s)\\ y(s,0)=0\\ u(s,0)=e^{-x^2}\Rightarrow u=\frac{s^s}{2}+f_3(s)=e^{-s^2}\Rightarrow f_3(s)=e^{-s^2}-\frac{s^2}{2} \end{cases}$$
$$\boxed{u=x^2-\frac{y^2}{2}+e^{y^2-x^2}}$$
l)
$$\begin{cases} u_x+u_y=u^2\\ u(x,0)=h(x) \end{cases}$$
Sabemos que $\begin{cases} a=1\\ b=1\\ c=u^2 \end{cases}$, encontramos as funções associadas a t
$\begin{cases} \frac{du}{dt}=u^2\Rightarrow \frac{du}{u^2}=dt\Rightarrow \frac{u^{-1}}{-1}=t+f_1(s)\\ \frac{dx}{dt}=1\Rightarrow x=t+f_2(s)\\ \frac{dy}{dt}=1\Rightarrow y=t+f_3(s) \end{cases}$, aplicando a condição inicial
$\begin{cases} x(s,0)=x=s\Rightarrow x=f_2(s)=s\\ y(s,0)=0\Rightarrow y=f_3(s)=0\\ u(s,0)=h(x)=h(s) \end{cases}\Rightarrow x-y=s$
Substituindo o valor de s em u. obtemos
$$u(x,t)=h(x-y)$$
m)
$$\begin{cases} (x+y)u_x+(x-y)u_y=1\\ u(x,-x)=\frac{-1}{\sqrt{2}}\ln x \end{cases}$$

Sabemos que $\begin{cases}a=x+y\\ b=x-y\\c=1\end{cases}$, observando que os termos de $u_x,u_y$ dependem de x e y, avaliamos a relação entre eles.
$$\frac{dy}{dx}=\frac{x-y}{x+y}\Rightarrow (x+y)dy=(x-y)dx\Rightarrow \underbrace{xdy+ydx}_{d(xy)}+ydy-xdx=0\Rightarrow2xy+y^2-x^2=2f_1(s)$$
Usando a condição inicial
$\begin{cases}x(s,0)=s\\ y(s,0)=s\\ u(s,0)=\frac{-s^2}{2}-\frac{s^2}{2} +2s(-s)=-2s^2\end{cases}\Rightarrow s=\sqrt{-\frac{f_1(s)}{4}}$ , sabendo a expressão de $f_1$ para $x, y$ 
$$\boxed{u=\frac{-1}{\sqrt{2}}\ln \sqrt{-\frac{f_1(x,y)}{4}}=\frac{-1}{\sqrt{2}}\ln  \left[ \sqrt{\frac{-2xy+x^2-y^2}{4}} \right]}$$

n)
$$\begin{cases} u_x+xu_y=y-\frac{x^2}{2}\\ u(0,y)=y^2 \end{cases}$$
Sabemos que $\begin{cases} a=1\\b=x\\c=y-\frac{x^2}{2} \end{cases}$, encontramos a relação de $u_x$ com t, substituímos x na segunda e o mesmo com a terceira

$\frac{dx}{dt}=1\Rightarrow x=t+f_1(s)$ => $\frac{dy}{dt}=x=t+f_1(s) \Rightarrow y=\frac{t^2}{2}+f_1(s)t+f_2(s)$
$\frac{du}{dt}=y-\frac{x^2}{2}=\frac{t^2}{2}+tf_1(s)+f_2(s)-\frac{(t+f_1(s))^3}{6}+f_3(s)$
Aplicando a condição inicial
$$\begin{cases} x(s,0)=f_1(s)=0\Rightarrow x=t\\ y(s,0)=f_2(s)=s\\ u(s,0)=f_3(s)=s^2\Rightarrow u(s,t)=ts+s^2 \end{cases}$$
Encontrando s, isolando na equação de y
$y=\frac{x^2}{2}+s\Rightarrow s=y-\frac{x^2}{2}$
$$\boxed{u=x\left[ y-\frac{x^2}{2} \right]+\left[ y-\frac{x^2}{2} \right]^2}$$