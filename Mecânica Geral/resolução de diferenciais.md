- Aqui serão caracterizadas as equações dadas por
$$a_2\frac{d^2}{dt^2}+a_1\frac{dx}{dt}+a_0x=f(t)$$
em que $f(t)$ é uma [[Força]] atuando no sistema

Para um sistema com [[Massa-mola]] e [[Resistência do ar]], obtemos
$\displaystyle m\frac{d^2x}{dt^2}=\sum_{i=1}^n F_i=-kx-b\frac{dx}{dt}+f(t) \Rightarrow m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=f(t)$

Caso **Homogêneo**
$$a_2\frac{d^2}{dt^2}+a_1\frac{dx}{dt}+a_0x=0$$
- como temos que os termos precisam ser uma combinação linear de seus termos para que seja possível cancelar. Então supomos uma solução do tipo $x(t)=ce^{pt}$; $\displaystyle \frac{dx}{dt}=cpe^{pt}$; $\displaystyle \frac{d^2x}{dt^2}=p^2ce^{pt}$
- Substituímos a suposição na equação para encontrar as constantes
$$p^2+\frac{a_1}{a_2}p+\frac{a_0}{a_2}=0$$
Obtemos que $$p=-\frac{a_1}{2a_2}\pm \sqrt{\frac{a_1^2}{4a_2^2}-\frac{a_0}{a_2}}$$
Combinamos as soluções para obter a *geral*
$$\large x(t)=ce^{\left(-\frac{a_1}{2a_2}+ \sqrt{\frac{a_1^2}{4a_2^2}-\frac{a_0}{a_2}}\right)t}+ce^{\left(-\frac{a_1}{2a_2}- \sqrt{\frac{a_1^2}{4a_2^2}-\frac{a_0}{a_2}}\right)t}$$

- Retornando ao problema físico originário
$$p = -\frac{b}{2m}\pm \left(\frac{b}{2m}\right)^2-\frac{k}{m}$$
**Definição**
$\displaystyle \gamma = \frac{b}{2m}$ e $\displaystyle \omega_0=\sqrt{\frac{k}{m}}$ => $p=-\gamma \pm \sqrt{\gamma^2-\omega_0^2}$  e obtemos
$$x(t)=e^{-\gamma t}(e^{\sqrt{\gamma^2-\omega_0^2}t}+ce^{-\sqrt{\gamma^2-\omega_0^2}t})$$

**Casos**
- $\Large \gamma<\omega_0,~~\gamma^2-\omega_0^2<0$, obtemos uma solução com [[Complexo]] 
	chamado de [[Amortecimento fraco]]
	**definimos** $\omega=\sqrt{\omega_0^2-\gamma^2}$, ou $\omega = i\sqrt{\gamma^2-\omega_2^2}$
	-> $p=\gamma \pm i\sqrt{\gamma^2-\omega_2^2}$
	=> a solução é da forma $x(t)= e^{\gamma}$
	$$x(t)=e^{-pt}(A\cos(\omega t)+B\sin(\omega t))$$
	ou
	$$x(t)=ce^{-\gamma t}\cos(\omega t -\theta)$$
	Para encontrar as constantes, precisamos de $\displaystyle x(0)=x_0~~e~~\frac{dx}{dt}(0)=v_0$ => $A=x_0$ e $\displaystyle B=\frac{v_0+\gamma x_0}{\omega}$ 
	
```functionplot
---
title: Função que descreve o movimento
disableZoom: false
bounds: [0, 5, -5, 5]
grid: true
xLabel: x
yLabel: y
---

f(x) = E^(-0.8*x)*cos(9*x)

```

- $\Large \gamma>\omega_0,~~\gamma^2-\omega_0^2>0$, obtemos uma solução real
	chamado de [[Amortecimento forte]]
	$$x(t)=c_1e^{-\gamma_1 t}+c_2e^{-\gamma_2 t}$$
	considero o ponto $x(0)=x_0=c_1+c_2$ e $v(0)=v_0=-\gamma_1 c_1-\gamma_2c_2$ 
	Portanto
	$\displaystyle c_2=\frac{v_0+\gamma_1 x_0}{\gamma_1 -\gamma_2}$ e $\displaystyle c_1=\frac{-(v_0+\gamma_2 x_0)}{\gamma_1 -\gamma_2}$ 

```functionplot
---
title: Função que descreve o movimento
disableZoom: false
bounds: [0,5,-5,5]
grid: true
xLabel: x
yLabel: y
---
f(x) = (E^(-x))

```
- $\Large \gamma=\omega_0,~~\gamma^2-\omega_0^2=0$, obtemos uma solução constante
	chamado de [[Amortecimento crítico]]
	Então, $x(t)=\underbrace{c}_{A+Bt}.e^{-pt}$ para que precise de $v_0$  
	$$x(t)=(x_0+(\gamma x_0+v_0)t)e^{-\gamma t}$$

```functionplot
---
title: Função que descreve o movimento
disableZoom: false
bounds: [0,5,-5,5]
grid: true
xLabel: x
yLabel: y
---
f(x) = (1+(2)*x)*(E^(-x))

```




