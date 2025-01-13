$$L=\frac{1}{2}m_s \dot {\vec  r_s}^2+\frac{1}{2}m_p\dot {\vec r_p}^2-V(|\vec r_p -\vec r_s|)$$
Sabemos que 
$m_s \dot{\vec r_s}+m_p\dot{\vec r_p}=\vec P=constante=M\vec R$
$\displaystyle \text{Definindo}\begin{cases} \vec R= \frac{m_s\vec r_s + m_t\vec r_t}{m_s+m_t}\\ \vec r=\vec r_p -\vec r_s \end{cases}\Rightarrow T=\frac{m_s \dot{\vec r}^2}{2}+\frac{m_t \dot{\vec r_t}^2}{2}=\frac{\vec P^2}{2M}+\frac{1}{2}\underbrace{\left( \frac{m_sm_p}{m_a+m_p} \right)}_{\text{m massa reduzida}}\dot r^2$


Conservação do [[Momento linear]] reduz a [[Lagrangiana]] para $\displaystyle L=\frac{1}{2}m\dot r^2 -V(r)$ 
Conservação do [[Momento angular]] :  $\vec L = l_z \hat z\Rightarrow \begin{align} \vec r . \vec L=0\\ \vec p . \vec L=0 \end{align}\Rightarrow$ Ponto de massa m se move no [[Plano]] $xy$

$\begin{align} x=r\cos \theta \\ y=r\sin \theta\end{align}\Rightarrow \dot x^2+\dot y^2=\dot r^2+r^2\dot \theta^2$
$$L=\frac{1}{2}m(\dot r^2 +r^2\dot \theta^2)-V(r)$$
usando a [[Equação de Euler-Lagrange]] para resolver
$\theta : \frac{d}{dt}\left( \frac{\partial L}{\partial \dot \theta} \right)-\underbrace{\frac{\partial L}{\partial \theta}}_{0}=0=\frac{d}{dt}(mr^2\dot \theta)\Rightarrow l_z=mr^2\theta$ sendo $l_z$ uma constante
$r: \frac{d}{dt}\left( \frac{\partial L}{\partial \dot r} \right)-\frac{\partial L}{\partial r}=\frac{d}{dt}(m\dot r)-\left( mr \theta^2 -\frac{\partial V(\dot r)}{\partial r} \right)=0$
$m\ddot r -mr\left( \frac{l_z}{mr^2} \right)^2+\frac{\partial V}{\partial r}=0$
$$m\ddot r - \frac{l_z^2}{mr^3}+\frac{dV}{dr}=0 ~~:\text{Equação de movimento em uma coordenada}$$ [[Energia]] é conservada => $E=T+V$
$E=\frac{1}{2}m(\dot r^2+ r^2\dot \theta^2)+V=\frac{1}{2}m\dot r^2 +\frac{l_z^2}{2m r^2}+V(r)=E$
$\dot r^2 =\left(\frac{dr}{dt}\right)^2=\frac{2}{m}\left( E-V-\frac{l_z^2}{2mr^2} \right)$
$\displaystyle dt=\frac{dr}{\sqrt{\frac{2}{m}\left( E-V-\frac{l_z^2}{2mr^2} \right)}}\Rightarrow  d\theta =\frac{l_z}{mr^2}\frac{dr}{\sqrt{\frac{2}{m}\left( E-V-\frac{l_z^2}{2mr^2} \right)}}$  

Que é uma equação de [[Elipse]]
