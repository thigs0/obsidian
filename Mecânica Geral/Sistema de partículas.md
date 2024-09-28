
$\displaystyle \vec{F_v}=\vec{F_v^{ext}}+\sum\limits{\vec{F_v}}_{v_k\lambda}$

- Se a [[3º Lei de Newton]] for válida 
$\sum\limits_{v} \vec{F_{v}} = \sum_{v} \vec F_v^{ext}=\vec F{ext} = M\frac{d^2\vec R}{dt^2}$

##### Problemas de determinação de M e R
1) Duas massas pontuais
2) Distribuição linear
$\lambda(x)$ é a [[densidade]] linear de massa => $d m(x)=dx\lambda(x)$

3) Distribuição Semi-circulo
$da=(d\theta r)dr$; $dm=da\sigma=drd\theta r\sigma$
4) hemisfério com densidade constante $\rho$
![[hemisfério.png|300]]
$M=\frac{\rho2\pi a^3}{3}$ 

$dv=(d\phi r \sin(\theta))(d\theta r)dr$
$dv = dr d\theta d\phi r^2\sin(\theta)$
$dxdydz=\frac{\partial (x,y,z)}{\partial \phi,\theta,r}drd\theta d\phi$

- calculo do centro de massa
$z_{cm}=\frac{1}{M}\int dm\times z=\frac{\rho 2\phi}{M}\int_0^a dr r^3 \in_{0}^{\phi/2}\theta \sin(\theta)\cos(\theta)$
Quando $\begin{cases}du=d\theta \cos(\theta)\\ u=\sin(\theta)\end{cases}$
$z_{cm}=\frac{2\pi\rho}{M}\frac{a^4}{4}\int_{0}^1duu=\frac{\pi \rho a^4}{4M}=\frac{3a}{8}$



##### Energia de um sistema de muitas partículas

$\vec F_v=\frac{d}{dt}(m_v\dot{\vec r_v })=\vec F_v^{exp}+\sum\limits_{\lambda}\vec F_{v,\lambda}$     
faça o produto escalar com $\dot{\vec r_v}$ 
$\dot{\vec r_v} . \frac{d}{dt}(m_v\dot{\vec r_v})=\frac{d}{dt}(\frac{1}{2}m_v\dot{\vec r_v})=\frac{d}{dt}T_v$ 
Do outro lado
$\vec F_v^{ext}.\dot{\vec r_v}+\sum\limits_v \vec F_{v,\lambda}.\dot{\vec r_v}=\frac{d}{dt}T_v$
...

##### Hipótese sobre as forças externas
$F_v^{ext}=-\nabla_v V^{ext}$ ; $v$ são as coordenadas do sistema

$W^{ext}=-\sum\limits_v \int d\dot{\vec r_v}.\nabla_v V^{ext}=-\sum\limits_v\int dV_v^{ext}=-\sum\limits_v (V_v^{ext}(t_2)-V_v^{ext}(t1))$
=> $W^{ext}=V^{ext}(t_1)-V^{ext}(t_2)$

##### Hipótese sobre força interna
1) São conservativas
2) São centrais