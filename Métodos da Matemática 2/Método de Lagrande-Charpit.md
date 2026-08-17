O problema principal é resolver uma [[EDP]] de primeira ordem, possivelmente não linear
tome $p=u_x,~~~q=u_y$ e uma EDP qualquer, renomeamos as variáveis e igualamos a zero para obter uma funcao $f(x,y,u,p,q)=0$
Usando a regra da cadeia obtemos
$$\begin{align}\frac{\partial f}{\partial x}=f_x+f_up+f_pp_x+f_qq_x=0\\ \frac{\partial f}{\partial x}\phi_x+\phi_up+\phi_pp_x+\phi_qq_x=0\\ \frac{\partial f}{\partial y}=f_y+f_yq+f_pp_y+f_qq_y=0\\ \frac{\partial f}{\partial y}=\phi_y+\phi_uq+\phi_pp_y+\phi_qq_y=0\end{align}$$
Podemos agora usar as duas primeira para eliminar $p_x$ e as duas últimas para eliminar $q_y$
obtemos uma edp quase linear e usamos o [[Método das características]]

$$\frac{dx}{-f_p}=\frac{dy}{-f_q}=\frac{du}{-pf_q-qf_q}=\frac{dp}{f_x+pf_u}=\frac{dq}{f_y+qf_u}=\frac{d\phi}{0}$$
