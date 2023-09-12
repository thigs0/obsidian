Podemos olhar o [[Teorema do valor médio]] na forma de integral 
$$\frac{1}{\epsilon}\int_a^{a+\epsilon}g(t)dt=g(\xi)$$
Como fora do intervalo é 0, temos:
$\displaystyle \int_0^\infty d_{a, \epsilon}(t)g(t)dt$ ,Tomamos o limite $\displaystyle \lim_{\epsilon \to 0} \int_0^\infty d_{a, \epsilon}(t)g(t)dt =\int_0^\infty \delta_a(t)g(t)dt$  

e temos que o delta de dirac irá realizar uma operação na função g(t)

$\displaystyle \int_o^\infty e^{-st}\delta_a (t)= e^{-as}$ ->> $\mathscr{L}\{\delta_a(t)\}= e^{-as}$  


--> _A função degrau_ <--
O [[Delta de Dirac]] é a derivada da [[Função degrau]]
$u_a(t)$ -> $\displaystyle \frac{d}{dt}u_a = \delta_a (t)$ 


$$Ax''+Bx'+Cx = \delta_a,~x(0)=0,~~ x'(0)=0$$
$Ax''_{\epsilon} + Bx'_{\epsilon}+ x_{\epsilon}= d_{a,\epsilon}(t)$ ==> Aplicamos a [[Transformada de Laplace]] 
$\displaystyle As^2X_\epsilon (s)+BsX_\epsilon (s)+CX_\epsilon (s) = \frac{1}{\epsilon}\frac{e^{-as}}{s} - \frac{-(a+\epsilon)s}{s}$
 $\displaystyle X_\epsilon (As^2 +Bs+c)= e^{-as}\left( \frac{1 - e^{-\epsilon s}}{\epsilon s}\right)$ 
 $\displaystyle X_\epsilon = \frac{e^{-as}}{as^2+bs+c}\left( \frac{1-e^{-\epsilon s}}{\epsilon s}\right)$, queremos o [[Limite]] quando $\large \epsilon$ tende a 0
 $\displaystyle \frac{e^{-as}}{as^2+bs+c} \lim_{\epsilon \to 0} \left( \frac{1-e^{-\epsilon s}}{\epsilon s}\right)$, usamos [[L'Hôpital]] temos que o limite é 1
 
 _Exemplo_:
	 $\displaystyle x'' +x= A \delta_{\pi /2}(t)$, esta equação é de uma [[Massa-mola]] com uma impulso momentâneo em $\displaystyle \frac{\pi}{2}$ 
	 $s^2X -sx(0) -x'(0)+X= Ae^{-\pi /2 s}$ -> $\displaystyle (s^2+1)X= s+Ae^{-s\pi /2}$ -> $\displaystyle X = \frac{s}{s^2+1}+ \frac{Ae^{-s \pi /2}}{S^2+1}$ 
	Aplicamos a inversa
	x(t) = $cos(t)+A u_{\pi /2}sen(t-\pi /2) = cos(t) -A u_{\pi /2}(t) cos(t)$ 



[[Princípio de Duhammel]]
