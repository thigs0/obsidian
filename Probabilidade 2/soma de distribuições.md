| Distribuição 1            | Distribuição 2            | Soma                                   | subtração                              | produto    | Produto contante C    |
| ------------------------- | ------------------------- | -------------------------------------- | -------------------------------------- | ---------- | --------------------- |
| $N(\mu_1,\sigma^2_1)$     | $N(\mu_2,\sigma^2_2)$     | $N(\mu_1+\mu_2,\sigma^2_1+\sigma^2_2)$ | $N(\mu_1-\mu_2,\sigma^2_1+\sigma^2_2)$ | $\chi^2_v$ | $N(C.\mu,C.\sigma^2)$ |
| $Bin(m_1,p)$              | $Bin(m_2,p)$              | $Bin(m_1+m_2,p)$                       |                                        |            |                       |
| $\chi^2_{v_1}$            | $\chi^2_{v_2}$            | $\chi^2_{v_1+v_2}$                     |                                        |            |                       |
| $Gamma(\alpha_1,\lambda)$ | $Gamma(\alpha_2,\lambda)$ | $Gamma(\alpha_1+\alpha_2,\lambda)$     |                                        |            |                       |
| $Exp(\lambda_1)$          | $Exp(\lambda_2)$          | $Gamma(2,\lambda)$                     |                                        |            |                       |
| $Ber(p)$                  | $Ber(p)$                  | $Bin(2, p)$                            |                                        |            |                       |
| $Poisson(\lambda)$        | $Poisson(\lambda)$        | $Poisson(\lambda_1+\lambda_2)$         |                                        |            |                       |
| $U(0,1)$                  | $U(0,1)$                  | $Triangular(0,1,2)$                    |                                        |            |                       |

X~Bernoulli (p)
Y~Bernoulli (p)
são independentes
##### Soma de [[Distribuição de Bernoulli]]
Em geral $Z=\sum\limits_{i=1}^n X_i$ ~ Binomial (n, p)
##### Soma de [[Distribuição binomial]]
**Exemplo**
X ~ Bin (n,p) e Y ~ Bin (m,p)
Vamos mostrar Z = X + Y ~ Bin (n+m,p)

$P(Z=z)=P(X+Y=z)=\sum\limits{y=0}^m P(X+Y=z,Y=y)=\sum\limits{y=0}^z P(X=z-y,Y=y)$
$=\sum\limits{y=0}^z\begin{pmatrix}n\\ z-y\end{pmatrix}p^{z-y}(1-p)^{n-(z-y)}.\begin{pmatrix}m\\ y\end{pmatrix}p^y(1-p)^{m-y}=\left[ \sum\limits{y}^z \begin{pmatrix}n\\ z-y\end{pmatrix}  \begin{pmatrix} m\\ y \end{pmatrix}\right].p^z(1-p)^{n+m-z}=\begin{pmatrix}n+p\\z\end{pmatrix}p^z(1-p)^{n+m-z}$ 
##### Soma de [[Distribuição Gama]]
X ~ $Gama(\alpha, \lambda)$ e Y ~ $Gama(\beta,\lambda)$ independentes
Z = X + Y ~ $Gama(\alpha+\beta,\lambda)$

$f_z(z)=\int_{-\infty}^{\infty} f_x (z-y)f_y(y)dy=\int_0^\beta \frac{\lambda^{\alpha-1}}{\Gamma{x}}(z-y)^{\alpha-1}e^{-\alpha (z-y)}\frac{\lambda^{\beta-1}}{\Gamma{\beta}}y^{\beta-1}e^{-\lambda y}dy$
$=\frac{\lambda^{\lambda+\beta-z}}{P(\alpha)\Gamma(\beta)}e^{-\lambda z}\int_0^z (z-y)^{\alpha -1}y^{\beta-1}dy$ 


=> $Z=X+Y$ ~  $Gama(\alpha+\beta,\lambda)$   
De maneira geral 
$x_i,...x_n$ independentes tal que $X_i$ ~ $Gama(\alpha_i,\lambda)$, i=1,...,n
1) $z=x_1+...+x_n=\sum\limits{i=1}^n X_i$ ~ $Gama\left( \sum\limits_{i=1}^n \alpha_i,\lambda \right))$
2) $X_i$ ~ $exp(\lambda)~~i=1,...,n~~exp(\lambda)=Gama(1,\lambda)$
3) $X_i$ ~ $\xi_{v_i}^2,~~i=1,...,n$  $Z=\sum\limits_{i=1}^n X_i$ ~ $\xi_{v}^2,~~v=\sum\limits{i=1}^n v_i$
[[Produto de distribuição normal]]
Demonstração: Se $X \sim N(0,1)$, então $X^2 \sim \chi^2_1$
[[Função de distribuição acumulada]] de $Y = X^2$

Para $y \ge 0$:
$$
F_Y(y) = P(Y \le y) = P(X^2 \le y) = P(-\sqrt{y} \le X \le \sqrt{y}).
$$

Como $X \sim N(0,1)$:
$$
F_Y(y) = \Phi(\sqrt{y}) - \Phi(-\sqrt{y}),
$$
onde $\Phi$ é a CDF da normal padrão.

Usando a simetria $\Phi(-z) = 1 - \Phi(z)$:
$$
F_Y(y) = \Phi(\sqrt{y}) - [1 - \Phi(\sqrt{y})] = 2\Phi(\sqrt{y}) - 1.
$$
2. Função densidade de probabilidade (PDF)

Derivando em relação a $y$:
$$
f_Y(y) = \frac{d}{dy} \left[ 2\Phi(\sqrt{y}) - 1 \right] = 2 \cdot \phi(\sqrt{y}) \cdot \frac{1}{2\sqrt{y}},
$$
onde $\phi(z) = \frac{1}{\sqrt{2\pi}} e^{-z^2/2}$ é a PDF da normal padrão.

Então:
$$
f_Y(y) = \frac{1}{\sqrt{y}} \cdot \phi(\sqrt{y}) = \frac{1}{\sqrt{y}} \cdot \frac{1}{\sqrt{2\pi}} e^{-y/2}.
$$

Simplificando:
$$
f_Y(y) = \frac{1}{\sqrt{2\pi y}}  e^{-y/2}, \quad y > 0.
$$

3. Identificação com a distribuição qui-quadrado

A PDF da distribuição $\chi^2_k$ é:
$$
f(y) = \frac{1}{2^{k/2} \Gamma(k/2)}  y^{k/2 - 1} e^{-y/2}, \quad y > 0.
$$

Para $k = 1$:
$$
\Gamma(1/2) = \sqrt{\pi},
$$
$$
f(y) = \frac{1}{2^{1/2} \sqrt{\pi}}  y^{-1/2} e^{-y/2} = \frac{1}{\sqrt{2\pi y}}  e^{-y/2}.
$$

Que é exatamente a PDF obtida para $Y$.

Conclusão
$$
\boxed{X^2 \sim \chi^2_1}
$$