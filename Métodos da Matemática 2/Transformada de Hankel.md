É um caso particular da [[Transformada de Fourier]]

## Caso de ordem 1, transformada de Bessel
Consider the base function $f(r,\theta)$ e $F(\rho, \phi)$ are periodic over $2\pi$ interval, at variables $\theta, \phi$. So rewrite the functions like
$$F(r,\theta) = \sum\limits_{n=-\infty}^\infty f_n(r)e^{in\theta} \hspace{5mm}   F(\rho,\phi)=\sum\limits_{n=-\infty}^\infty F_n(\rho)e^{in\phi}$$
....

$$\begin{align}  F_n(\rho) i^n\int_0^\infty rJ_n(\rho r)f_n(r)dr\\ f_n(r)=(-i)^n  \int_{0}^{\infty} \rho J_n(\rho r)F_n(\rho)d\rho\end{align}$$

## Transformada de Hankel de ordem $\mu$

$$\begin{align} \mathscr{H}_\mu[f(x)]=F(k)=\int_0^{\infty} xf(x)J_\mu (kx)dx\\\mathscr{H}_\mu[F(k)]=f(x)=\int_0^\infty kF(k)J_\mu(xk)dk \end{align}$$