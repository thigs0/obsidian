Essa transformada surge a partir de uma mudanca de variável na [[Transformada de Laplace]].

Mudando
$$\begin{cases}ik=s\\x=\ln \xi\end{cases}\Rightarrow \begin{cases} \mathscr{M}[f(x)]=F(s)=\displaystyle\int_0^\infty x^{s-1}\underbrace{f(x)}_{\displaystyle \frac{g(\ln \xi)}{\sqrt{2\pi}},~~\xi \rightarrow x}dx\\ \mathscr{M}^{-1}[F(s)]=f(x)=\displaystyle \frac{1}{2\pi i} \int_{\gamma-i\infty}^{\gamma+i\infty}x^{-s}\underbrace{F(s)}_{G(-is)}ds\end{cases} $$

### Exemplo
Seja $f(x)=e^{-\alpha x},~~\alpha>0$. Então
$$F(s)=\int_0^\infty e^{-\alpha x}x^{s-1}dx=\frac{1}{\alpha^s}\int_0^\infty e^{-y}y^{s-1}dy=\frac{\Gamma(s)}{\alpha^s}$$
Onde Re(s) > 0. Como a [[Função gama]] tem polos simples nos inteiros negativos. Tome um cemi-círculo na parte positiva
$$e^{-\alpha x} = \frac{1}{2\pi i}\int_{\gamma-i\infty}^{\gamma+i\infty} x^{-s}\frac{\Gamma(s)}{\alpha^s}ds=\sum\limits_{k=0}^{\infty}  [(\alpha x)^{-s}\Gamma(s)]=\sum\limits_{k=0}^{\infty} (\alpha x)^k \frac{(-1)^k}{k!} $$
que é conhecida como [[Integral de Cahen-Mellin]]

### Propriedades
1. $\mathscr{M}[f(ax)]=a^{-s}F(s)$
2. $\mathscr{M}[f(1/x)]=F(-s)$
3. $\mathscr{M}[xf(x)]=F(s+1)$
4. $\mathscr{M}[xf'(x)]=-sF(x)$
