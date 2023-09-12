- Seja $W \subset \mathbb{R}^3$, dim E = 3, $\partial E = S$ - Orientada positivamente para fora $\Omega$ aberta, $\vec F \in C^1(\Omega)$

$$\iint_S \vec F \cdot \vec n ds = \iiint_W div(\vec F)dV$$
A integral da superfície com fronteira S e o interior da superfície fechada

## Hipóteses 
--> Superfície fechada
--> Orientada positivamente ; Normal apontando para fora
--> Sem singularidade ; Campo contínuo

**Exemplo**
Seja E - Região limitada pelo cilíndro parabólico $z=1-x^2$ e os planos z=0, y=0, y+z=z
![[exemplo_gauss.png]]
Calcule o fluxo de $\displaystyle \vec F = (xy, y^2+e^{xz^2}, sen(xy))$ 
$\displaystyle \nabla \vec F = \frac{\partial xy}{\partial x}+\frac{\partial y^2+e^{xz^2}}{\partial y}+\frac{\partial sen(xy)}{\partial z} = y+2y+0=3y$

Fluxo -> $\displaystyle \iiint _E 3ydV$, E{(x,y,z)| $-1 \leq x\leq 1, 0 \leq z \leq 1-x^2, 0\leq 2-z$}

= $\displaystyle 3\int_{-1}^1\int_0^{1-x^2}\int_0^{2-z}ydydzdx =\frac{184}{35}$


