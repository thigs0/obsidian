**Método das aproximações sucessivas ou [[Método de iteração Picard]]**

temos a equação diferencial $s' = f(t,s)$
a [[Integral]] de forma $\displaystyle \int_0^t s'$
e definimos uma função que se aproxime de s como $\large \phi$
$\int f(s,\phi)$ e podemos aproximar $\large \phi_0 =0$ e obter
$\displaystyle \phi_1 = \int_0^t f(s,\phi_0)ds$
e seguimos este passo n vezes na forma 
$$\phi_{n+1}(t) = \int_0^tf(s,\phi_n)ds$$
1. A sequência precisa convergir
	Para isso estimamos $|\phi_{k+1}(t)-\phi_k(t)|$ do termo geral
2. Cada passo precisa existir
