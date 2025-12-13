Sejam $X_1,X_2$ variáveis aleatórias e $S_1,S_2$ suas somas parciais
$$\frac{S_n-\mathbb{E}S_n}{n}\xrightarrow{\mathbb{P}} 0$$
Outra formulação

Seja $X_1,X_2,...$ uma sequência de variáveis aleatórias independentes e identicamente distribuídas, cada uma com média finita $E[X_i]=\mu$. Então, para qualquer $\epsilon>0$
$$P\left[|\frac{X_1+X_2+...+X_n}{n}-\mu|\geq \epsilon\right]\to 0,~~~\text{quando  }n\to\infty$$
**Demonstração**
Vamos demonstrar o teorema com a única hipótese adicional de que as variáveis possuam uma variância finita $\sigma^2$.
$P\left[\frac{X_1+...+X_n}{n}\right]=\mu$ e $Var\left(\frac{X_1+...+X_n}{n}\right)=\frac{\sigma^2}{n}$
pela [[Desigualdade de Chebyshev]]
$P\left[|\frac{X_1+...X_n}{n}-\mu|\right]\geq \epsilon]\leq \frac{\sigma^2}{n\epsilon^2}$, quando $n\to\infty\Rightarrow \lim_{n\to\infty} P\left[ \left| \frac{X_1+X_2+...+X_n}{n} -\mu\right| \geq \epsilon\right]\leq \delta$ com delta incrivelmente pequeno  




[[Lei dos grandes números de Bernoulli]]
Considere uma sequência de ensaios independentes tendo probabilidade  de sucesso em cada ensaio. Se $S_n$ é o número de sucessos nos primeiros  ensaios, então
$$\frac{S_n}{n}\xrightarrow{\mathbb{P}} p$$

[[lei dos grandes números de Tchebyshev]]
Sejam $X_1,X_2,...$ variáveis aleatórias não-correlacionadas. Suponha que existe M finito tal que  $\mathbb{V}X_n< M$ para todo . Então
$$\frac{S_n-\mathbb{E}S_n}{n}\xrightarrow{\mathbb{P}}0$$
