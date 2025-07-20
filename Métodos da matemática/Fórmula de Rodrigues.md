$$\frac{1}{\sqrt{1-2xt+t^2}}=\sum\limits_{n=0}^\infty P_n(x)t^n $$
##### Para os [[polinômio de legendre]] 
transformamos a equação em uma [[Integral de linha]] ao redor da origem $\oint \frac{t^{-m-1}dt}{\sqrt{1-2xt+t^2}}=\sum\limits_{n=0}^\infty P_n (x)\oint t^{n-m-1}dt$
usamos então a [[Integral de Cauchy]] para obter $2\pi iP_m(x)=\oint_c \frac{t^{-m-1}}{\sqrt{1-2xt+t^2}}$
Definimos que $\sqrt{1-2xt+x^2}=1-yt\Rightarrow \begin{cases} t=\frac{2(x-y)}{1-y^2},t=0\Rightarrow y=x\\ dt=\frac{2}{1-y^2}dy+\frac{4y(y-y)}{(1-y^2)^2}dy \end{cases}$


$$P_n(x)=\frac{1}{2^n}\frac{1}{n!}\frac{d^n}{dx^2}[(x^2-1)^n]$$
