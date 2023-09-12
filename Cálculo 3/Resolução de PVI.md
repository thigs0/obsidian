- _Construir um gráfico de direções_
```python
import matplotlib.pyplot as plt
import numpy as np
from scipy.integrate import odeint

# define a equacao
def f(y,x): return x+2*y

# discretriza o dominio e resolve para 0<x<2
xs = np.linspace(0,2,100)
ys = odeint(f,1,xs)
plt.plot(xs,ys, 'b', linewidth=2)

# discretriza o dominio e resolve para -2<x<0
xs = np.linspace(0,-2,100)
ys = odeint(f,1,xs)
plt.plot(xs,ys, 'b', linewidth=2)

# plota eixos
plt.axhline(y=0, c="black")
plt.axvline(x=0, c="black")

# campo de direcoes
x = np.linspace(-2,2,100)
y = np.linspace(-2,2,100)
X, Y = np.meshgrid(x, y)
dy = X+2*Y
dx = np.ones(dy.shape)
plt.streamplot(X,Y,dx, dy)


# plota tudo
ax = plt.gca()
ax.set_ylim(-2,2);

```
```mathematica
StreamPlot[{1,x+2y},{x,-2,2},{y,-2,2}]
```

Dado um problema na forma
$y'(x)+p(x)y(x) = f(x)$

Temos diretamente 
	 [[Método do fator integrante]]
		Existe uma função pela qual multiplicamos toda a equação e a solução é obtida de forma rápida
		chamamo fator integrande de $\displaystyle u(x) = e^{\int p(x)dx}$
		e a equação fica na forma:
		$\displaystyle u(x)y'(x)+ u(x)p(x)y(x)= u(x)f(x) = \frac{d}{dx}[u(x)y]$
		- Exemplos
			1. $y'-2xy=e^{x^2}$; 
			como $\displaystyle u(x) = e^{\int(p(x)dx)} = e^{\int-2xdx}= e^{-x^2}$; fixamos a constante que aparece na integral como c=0 
			$e^{-x^2}y' -2xe^{-x^2}y = e^{-x^2} e^{x^2} = \frac{d}{dx}\left[ e^{-x^2}y\right]$; integramos em relação a x
			$\displaystyle \int \frac{d}{dx}\left[ e^{-x^2}y\right] = \int e^{0} \Rightarrow e^{-x^2}y=x \Rightarrow y = xe^{x^2}$
			
	[[Equações separáveis]]
		Caso a função possa ser separada em dois lados, um só com termos de y e outro só com termos de x. Então, podemos integrar ambos os lados em relação a x
		- Exemplo
			1. $\displaystyle y' = \frac{y(y+1)}{y(x-1)}$
			isolamos e integramos, $\displaystyle \frac{y'y}{y(y+1)}= \frac{1}{x-1} \Rightarrow \frac{dy}{dx}\frac{y}{y(y+1)}= \frac{1}{x-1} \Rightarrow \int\frac{dy}{dx}\frac{y}{y(y+1)} dx=\int \frac{1}{x-1}dx$
			$\int \frac{dy}{(y+1)} = \int \frac{1}{x-1}dx \Rightarrow Ln(y+1)=Ln(x-1)$
			$y=x-2$; Está é a solução para o sistema
			
	[[Equação de Bernouli]]
		Dada uma função em y, podemos criar uma função v(y(x)) que seja facilmente integravel e assim retornamos para y(x). O nome é em honra a [[Jakob Bernoulli]]
		para o modelo não linear: $$y' + p(t)y=q(t)y^n$$ Deixando apenas os termos de x ao lado direito.
		$y^{-n}y' + p(t)y^{n-1}=q$
		Criamos uma nova função dada por: $v(t) = y^{1-n}$
		Assim a derivada de v é: $v'(t) = (1-n)y^{-n}y'$
		Observamos que: $\displaystyle \frac{v'}{1-n} = y^{-n}y'$; e este é o termo que aparece na equação. Assim retornamos com essa nova variável e obtemos: 
		$\displaystyle \frac{v'}{1-n} + p(t)v(t) = q$
		e esta equação agora é linear e podemos aplicar o método do mator integrante
		.
		Exemplo
			1.  $x^2 y'+2xy= 5y^4$
			Deixamos na forma simples: $\displaystyle y' + 2x^{-1}y = \frac{5y^4}{x^2}$; $x \neq 0$
			Deixamos apenas x do lado direito: $\displaystyle y^{-4}y' + 2x^{-1}yy^{-4}=\frac{5}{x^2} = y^{-4}y'+2x^{-1}y^{-3}$
			Definimos v(x)= $y^{-3}$ e $v'(x) = -3y^{-4}y'$ 
			Substituimos: $\displaystyle -\frac{v'(x)}{3} + \frac{2}{x}v(x)= \frac{5}{x^2}$
			Simplificamos: $\displaystyle v'(x) -\frac{6}{x}v(x)= -\frac{15}{x^2}$
			Agora a equação é linear e conseguimos uma solução
			$\displaystyle u(x) = e^{-6\int x^{-1}} =e^{-6Ln(|x|)}= e^{Ln(|x|^{-6})}= x^{-6}$; Assumimos que x>0
			$\displaystyle v(x)x^{-6} = -15\int x^{-8}= \frac{15}{9}x^{-9} \Rightarrow v(x) =\frac{5}{3} x^{-3}$
			Retornamos de v(x) em y(x): $\displaystyle y^{-3}=\frac{5}{3}x^{-3} \rightarrow y= \sqrt[3]{\frac{3x^3}{5}}$ 
			E assim achamos a solução de y(x)

_Exemplo físico_
	-**Equação de verhulst ou equação logística**
	$$\frac{dy}{dt}=(r-ay)y ~~~~~~~~~~~ou~~~~~~~~~ \frac{dy}{dt}=r \left(1 - \frac{y}{K} \right)y$$
	