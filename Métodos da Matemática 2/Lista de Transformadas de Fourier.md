| f(x)          | F(x)                                                             | Propriedade |
| ------------- | ---------------------------------------------------------------- | ----------- |
| $\delta(x)$   | $\frac{1}{2\pi}$                                                 | (1)         |
| $\cos(x)$     | $\displaystyle \frac{\pi}{2}[\delta(k+\alpha)+\delta(k-\alpha)]$ | (2)         |
| $e^{-\|x\|}$  | $\displaystyle \sqrt{\frac{2}{\pi}}\frac{1}{1+k^2}$              | (3)         |
| $ae^{-\|x\|}$ | $a\displaystyle \sqrt{\frac{2}{\pi}}\frac{1}{1+k^2}$             | (4)         |



##### Propriedade 3
$$F[e^{-|x|}]=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}  e^{-|x|}e^{ikx}dx$$
$\displaystyle F[e^{-|x|}]=\frac{1}{\sqrt{2\pi}} \int_{-\infty}^\infty e^{ikx-|x|}dx=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty e^{ikx-ax}dx,~~a=\begin{cases} 1,x>0\\ -1,x\leq 0 \end{cases}$ 
$\displaystyle \frac{1}{\sqrt{2\pi}} \int_{-\infty}^\infty \underbrace{e^{-x(a-ix)}}_{\begin{align} -x(a-ik)=j\\ -dx(a-ik)=dj \end{align}}dx= \frac{-1}{\sqrt{2\pi}}\int_{\infty}^{-\infty}\frac{e^j}{a-ik}dj=\frac{-1}{\sqrt{2\pi}}\left[ \underbrace{\frac{1}{-1-ik}\int_{\infty}^0e^jdj}_{A} + \underbrace{\frac{1}{1-ik}\int_{0}^{-\infty} e^jdj}_{B}\right]$ 
$A=\frac{1}{-1-ik}e^{e^{-x(-1-ik)}}|_{\infty}^0=\frac{-1}{+1+ik}[1-0]=\frac{-1}{+1+ik}$
$B=\frac{1}{1-ik}e^{-x(1-ik)}|_{0}^{-\infty} =\frac{1}{1-ik}[0-1]=\frac{-1}{1-ik}$
$A+B=\frac{-2}{1+k^2}$
$$\boxed{F[e^{-|x|}]=\sqrt{\frac{2}{\pi}}\frac{1}{1+k^2}}$$


