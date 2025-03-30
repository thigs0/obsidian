Para exemplificar usaremos a [[Equação da onda]] $\displaystyle \frac{d^2}{dt^2}-c^2\Delta^2 u=0$ 

1) Em [[coordenadas cartesianas]] temos $\frac{1}{c^2}\frac{\partial^2u}{\partial t^2}-\left( \frac{\partial^2u}{\partial x^2}+\frac{\partial^2u}{\partial y^2}+\frac{\partial^2u}{\partial z^2}   \right)=0$
	- usamos uma solução do tipo $u(t,x,y,z)=T(t)X(x)Y(y)Z(z)$ e obtemos $X(x)Y(y)Z(z)\frac{T''}{c^2}=TYZX''+TXZY''+TXYZ''$
2) Dividimos por $TXYZ$ e obtemos $\frac{T''}{c^2T}=\frac{X''}{X}+\frac{Y''}{Y}+\frac{Z''}{Z}$ 

Em [[Coordenadas esféricas]] 
- Usaremos $u(t,r,\theta,\phi)=T(t)R(r)\Phi(\phi)\Theta(\theta)$ 
- aplicando na equação da onda, obtemos $R\Phi\Theta\frac{T''}{c^2}=\frac{1}{r^2}\frac{\partial }{\partial r}\left(r^2\frac{\partial }{\partial r}(TR\theta\phi)\right)+ \frac{1}{r^2sen(\theta)}\frac{\partial }{\partial \theta}\left( sen(\theta)\frac{\partial}{\partial \theta}(TR\Theta\Phi) \right)+\frac{1}{r^2sen^2(\theta)}\frac{\partial^2}{\partial \phi^2}(TR\Theta\Phi)$ 
- -> $\displaystyle \frac{T''}{c^2T}=\frac{1}{r^2R}\frac{d}{dr}\left(r^2\frac{dR(r)}{dr}\right)+\frac{1}{r^2sen(\theta)}\frac{1}{\Theta}\frac{d}{d\theta}\left(sen(\theta)\frac{d}{d\theta}\Theta(\theta)\right)+\frac{1}{\Phi r^2sen(\theta)}\frac{d^2\Phi}{d\phi^2}$ 
e obtemos as equações
$$\begin{cases}T''+c^2\alpha^2T=0\\ \frac{d}{dr}\left( r^2\frac{dR}{dr}\right)+(\alpha^2r^2-\beta^2)R=0\\\frac{d^2\Phi}{d\phi^2}+\gamma^2\Phi=0\\ sen(\theta)\frac{d}{d\theta}\left( sen(\theta)\frac{d\Theta}{d\theta} \right)+(\beta^2sen^2(\theta)-\gamma^2)\Theta(\theta)=0\end{cases}$$

assim obtemos que a segunda é uma [[Equação de Bessel]], a quarta é uma [[Equação de Legendre]]