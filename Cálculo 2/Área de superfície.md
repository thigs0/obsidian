- Calcular área de uma superfície usando integral dupla $z=f(x,y)$
para um retângulo infinitesimal, a área do plano tangente é igual a área da função

definimos como : $\displaystyle A(s) =\lim_{m,n\to \infty} \sum\limits_{i=1}^m\sum\limits_{j=1}^n \Delta T_{ij}$
$\Delta \vec{T_{ij}} = [\vec a\times \vec b],~\vec a=f_x,\vec b=f_y$
$a=Axi+f_x(x_i,y_j)\Delta xk$
$b=\Delta yj+f_y(x_i,y_j)\Delta yk$
então:
$a\times b = \begin{vmatrix} i & j & k \\ \Delta x & 0 & f_x(x_i,y_j)\Delta x \\ 0 & \Delta y  & f_y(x_i,y_j)\Delta y\end{vmatrix}$
$\Delta T_{ij}=\sqrt{[f_x(x_i,y_j)]^2+[f_y(x_i,y_j)]^2+\Delta A}$

- Definição geral de área
$\displaystyle A =\lim_{\Delta T\to 0} \Delta T_{ij}=\iint_D\sqrt{1+\left(\frac{\partial z}{\partial x}\right)^2 + \left(\frac{\partial z}{\partial y}\right)^2 dA}$
