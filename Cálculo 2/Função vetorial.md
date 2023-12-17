Uma função vetorial é um vetor em que suas componentes variam segundo uma [[função]]
###### Propriedades
- $\large \displaystyle \lim_{t\to a} [u(t)+v(t)]=\lim_{t\to a} u(t)+\lim_{t\to a}v(t)$
	**Demonstração**
	$u(t)+v(t)=k(t)\Rightarrow k(t)=(u_1+v_1,u_2+v_2,....,u_n+v_n)$
	$\lim_{t\to a} k(t) =\lim_{t\to a} \sum_{n=1}^i u_n+v_n = \sum_{n=1}^i \lim_{t\to a}(u_n+v_n)$ 
	$= \sum_{n=1}^i \lim_{t\to a}u_n +\lim_{t\to a}u_n=\sum_{n=1}^i\lim_{t\to a}u_n+\sum_{n=1}^i \lim_{t\to a}v_n$
	$= \lim_{t\to a}\sum_{n=1}^i u_n +\lim_{t\to a}\sum_{n=1}^i v_n = \lim_{t\to a}u(t)+\lim_{t\to a}v(t)$ 
- $\large \displaystyle \lim_{t\to a} c\cdot u(t) = c.\lim_{t\to a}u(t)$ 
	**Demonstração**
	$\lim_{t\to a} c\sum_{n=1}^n u_n = \lim_{t\to a}c\cdot \lim_{t\to a}\sum_{n=1}^i u_n=c\lim_{t\to a}\sum_{n=1}^i u_n$ 
	$=c\lim_{t\to a}u(t)$ 
- $\large \displaystyle\lim_{t\to a}[u(t).v(t)]=\lim_{t\to a}u(t).\lim_{t\to a}v(t)$
	 **Demonstração**
	 $u(t).v(t)=\sum\limits_{n=1}^i u_n.v_n\Rightarrow \lim_{t\to a}[u(t).v(t)]=\lim_{t\to a}\sum\limits_{n=1}^i u_n.v_n$ 
	 Se todo limite interno existe,então
	 $=\sum\limits_{n=1}^i \lim_{t\to 0}[u_n.v_n]=\sum\limits_{n=1}^i \lim_{t\to 0} u_n.\lim_{t\to a}v_n$ 
	 O limite das componentes multiplicado é o produto dos [[Limite]]s dos [[Vetor]]es 
- $\large \displaystyle \lim_{t\to a}[u(t)\times v(t)]=\lim_{t\to a}u(t) \times \lim_{t\to a}v(t)$ 

###### Limite de uma função vetorial
$$\lim_{t\to \infty} (\arctan t ,e^{-2t},\frac{\ln t}{t})=k$$
$\displaystyle \lim_{t\to \infty} x = \lim_{t\to \infty} \arctan t=\frac{\pi}{2}$
$\displaystyle \lim_{t\to \infty} y = \lim_{t\to \infty} = \lim_{t\to \infty} e^{-2t}=0$
$\displaystyle \lim_{t\to \infty} z = \frac{\ln t}{t}=\lim_{t\to \infty} = 0$

$\lim_{t\to \infty} k = (\pi/2,0,0)$

###### Derivada de uma função vetorial
$\displaystyle \frac{dr}{dt}=r'(t)=\lim_{h\to a} \frac{t(t+h)-r(t)}{h}$ -> $T(t)=\frac{r'(t)}{|r'(t)|}$
