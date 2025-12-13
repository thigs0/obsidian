Seja $x_1,x_2,...,x_n$ e $T_{n}$ é a média amostral de x. Seja g uma [[função]] com [[Derivada]] não nula
Se temos um problema 
$$\sqrt{n}(T_n-\theta)\xrightarrow D N(0,\theta^2)$$
Aplicando a função g
$$\sqrt{n}(g(T_n)-g(\theta))\xrightarrow D N(0, \sigma^2[g'(\theta)]^2)$$


**Exemplo**
Seja $x_1,x_2,...,x_n\sim exp(\theta)$, $g(x)=x(1-x)$, $g'(x)=1-2x$
$\sqrt{n}(\bar X(1-\bar X)- \frac{1}{\lambda}(1-\frac{1}{\lambda}))\xrightarrow D \displaystyle N(0,\frac{1}{\lambda}(1-2\frac{1}{\lambda})^2)$ 