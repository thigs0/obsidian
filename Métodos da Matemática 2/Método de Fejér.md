Seja $S_k(x)$ uma [[Cálculo 3/Sequência]] de somas parciais
$$S_k(x)=\sum\limits_{n=0}^ku_n(x),~~k=0,1,...,N-1$$
Obtemos o [[Teorema de Fejér]]
Seja $f(x)$ uma [[função]] contínua e periódica ($2\pi$)e seja $\sigma_N(x)$ a [[Soma de Cesàro]] da [[Séries de Fourier]]. Então a [[Cálculo 3/Sequência]] de funções $\sigma_N(x)$ converge para $f(x)$

**Demonstração**
Sabendo que o [[Núcleo de Dirichlet]] é dado por $D_N(u)=\displaystyle\frac{sen(N+1/2)u}{2\pi sen(u/2)}$, obtemos que a soma parcial série de Fourier $$S^N[f](x)=\int_{-\pi}^\pi D_N(\eta-x)f(\eta)d\eta$$

