[[Rotacional]] e [[Divergente]], são operações que podem ser realizadas com campos vetoriais.

### [[Divergente]]
$$div \vec F = \frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z} = \nabla.\vec F$$

**Teorema**
$\Delta f = \nabla^2f = \nabla\nabla f = div(grad~f)$ -Operador de Laplace  


### [[Rotacional]] 
---> Se $\vec F = P\hat i+ Q \hat j+ R \hat k$ é  um campo vetorial em R³ e as derivadas parciais de P,q e R existem, então o rotacional de F é o campo vetorial de R³ definido por:$$Rot~\vec F = \left( \frac{\partial R}{\partial y}- \frac{\partial Q}{\partial z}\right)\hat i + \left( \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x}\right)\hat j + \left( \frac{\partial Q}{\partial x}-\frac{\partial P }{\partial y}\right) \hat k$$

--> $\nabla$ é denominado operador diferencial vetorial
Quando ele opera em uma função escalar, gera o gradiente. Podemos pensar nele como o vetor $\displaystyle \nabla = \frac{\partial}{\partial x}\hat i+ \frac{\partial}{\partial y} \hat j+\frac{\partial }{\partial z}\hat k$ 
Assim, podemos imagina o produtor vetorial $$\nabla \times \vec F = \begin{vmatrix}  
i & j & k\\  
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z}\\
P & Q & R
\end{vmatrix}$$
Assim $Rot~\vec F = \nabla \times \vec F$ 

$\large \textbf{teorema}$ --> Se **F** é uma função de três variáveis  que tem [[Derivada]]s parciais de segunda ordem contínuas, então o rotacional do gradiente é zero:$$rot(\nabla f) = \vec 0$$ Como o campo $\vec F$ é conservativo de forma $\nabla f$. Então:
	Se $\vec F$ é conservativo, então rot $\vec F$ = 0

**Exercícios**:
$F(x,y,z)=y^2z^3\hat i+2xyz^3 \hat j+3xy^2z^2\hat k$
assim, $\nabla\times F(x,y,z)=\begin{vmatrix}i & j & k \\ \frac{d}{dx} & \frac{d}{dy} & \frac{d}{dz} \\ y^2z^3 & 2xyz^3 & 3xy^2z^2\end{vmatrix}$
$\displaystyle =\left(\frac{d}{dy}(3xy^2z^2)-\frac{d}{dz}(2xyz^3)\right)\hat i+\left(\frac{d}{dx}(3xy^2z^2)-\frac{d}{dz}(y^2z^3)\right)\hat j + \left(\frac{d}{dx}(2xyz^3)-\frac{d}{dy}(y^2z^3)\right)\hat k$ $=(2xyz^2-6xyz^2)\hat i+(3y^2z^2-3y^2z^2)\hat j+(2yz^3-2yz^3)\hat k$

