- Usaremos a [[Equação da onda]] $\nabla^2 u=\frac{1}{c^2}\frac{\partial ^2 u}{\partial t^2}$
- Deve se anular em a e b, $u(a,\theta,t)=u(b,\theta,t)=0$
- $u(r,2\pi,t)=u(r,0,t)$
- $u(r,\theta,0)=f(r,\theta)$
- $\frac{\partial u}{dt}u(r,\theta,t)|_{t=0}=g(r,\theta)$
Em coordenadas cilíndricas
$$\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial u}{\partial r}\right)+\frac{1}{r^2}\frac{\partial^2u}{\partial \theta^2}=\frac{1}{c^2}\frac{\partial^2u}{\partial t^2}$$
- Separando as variáveis, $u=R(r)\Theta(\theta)T(t)$
$\displaystyle \frac{1}{rR}\frac{d}{dr}\left( r\frac{dR}{dr} \right)+\frac{1}{r^2\Theta}\frac{d^2\Theta}{d\theta^2}=\frac{1}{c^2}\frac{T''}{T}=-\lambda$ , analisamos posteriormente $T''+\lambda^2c^2T=0$
$\frac{1}{R}r\frac{d}{dr}\left( r\frac{dR}{dr}\right)+\lambda^2r^2=-\frac{1}{\Theta}\Theta''=m^2$
$\Theta_m(\theta)=Am\cos(m\theta)+Bm\sin(m\theta)~~~\begin{cases}\Theta''+m^2\Theta=0\\ \Theta(0)=\Theta(2\pi)~\text{PSL periódico}\\ \Theta'(0)=\Theta'(2\pi)\end{cases}$
$fe~~\begin{cases}r^2R''+rR'+(\lambda^2r^2-m^2)R=0\\ R(a)=0=R(b)\\ R=CJ_m(\lambda r)+DY_m(\lambda r)\\ \lambda~satisfaz:~ \frac{J_m(\lambda b)}{Y_m(\lambda b)}=\frac{J_m(\lambda a)}{Y_m(\lambda a)}\Rightarrow \lambda mn,~~n=1,2,3,...\end{cases}$

E assim temos [[Equação de Bessel]]

Resolvendo no tempo
$\begin{cases}T''+\lambda^2_{mn}c^2T=0\\T(1)=E_{mn}\cos(\omega_{mn}t)+F_{mn}\sin(\omega_{mn}t),~~com~~ \omega_{mn}=\lambda_{mn}\end{cases}$ 
com modos normais
$u_{mn}(r,\theta,t)=\cos(\omega_{mn}t)[A_{mn}\cos(m\theta)+B_{mn}\sin(m\theta)].[J_m(\omega_{mnr})Y_m(\omega_{mna})-J_m(\omega_{mna})Y_{m}\cos(nr)]...$
