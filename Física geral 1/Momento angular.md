Se $mv$ é o momento linear => $I\omega$ é o momento angular

$$I\omega = (mr^2).\left(\frac{v}{r}\right) = mrv$$
$L = I\omega = mvr = [kg.m^2/s]$] -> Pode ter sinal positivo ou negativo, pois depende de $\theta$
$I$  é a [[Inercia rotacional]]

#### Momento angular de muitas partículas
$\vec L_v =\vec r_v\times \vec p_v$, $\vec L=\sum\limits_v \vec L_v$: momento angular total
$\frac{d\vec L}{dt}=\sum\limits_v (\vec r_v\times \vec F_v)=\sum\limits_v \vec r_v\times (\vec F_v^{ext}+\sum\limits_\lambda \vec F_{v,\lambda})$ 
somatório sobre forças internas:  $\sum\limits_{v,\lambda} \vec r_v\times \vec F_{v,\lambda}=\frac{1}{2}\sum\limits_{v,\lambda} (\vec r_v\times \vec F_{v,\lambda}+\vec r_{\lambda}\times \vec F_{\lambda,v})$ , temos $\vec F_{v,\lambda}=\vec F_{\lambda, v}$ 
$\vec L =\sum\limits_v m_v(\vec r_v\times \vec v_v)= \sum\limits_v m[(\vec R+\vec r_v')\times (\vec V=\vec v_v')]=(\sum\limits_v m_v)\vec R\times \vec V+\vec R\times \overbrace{\sum\limits m_v\vec v_v'}^{0}+ \overbrace{\sum\limits_v m_v\vec r_v}^{0}\times \vec V + \sum\limits_v m_v\vec r_v'\times v_v'$  
$\vec L=M\vec R\times \vec V+\sum\limits_v m_v\vec r_v'\times \vec v_v'$ 
[[Torque]] do sistema
$\frac{d\vec L}{dt}=\vec R\times M\frac{d\vec V}{dt}+\sum\limits_v m_v\vec r_v\times \frac{d\vec v_v'}{dt}=\vec \tau_{CM}+\vec \tau_{rel}$ 