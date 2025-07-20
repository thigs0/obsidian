- Consideramos as [[Funções de Bessel]], mas em um caso esférico
- A equação que analisamos é $x^2y''+2xy'+(x^2-n(n+1))y=0$
Resolvendo por [[Série de Frobenius]]
$y(x)=\sum\limits_{n=0}^\infty a_nx^{n+r};y'(x)=\sum\limits_{n=1}^\infty (n+r)x^{n+r-1}; y''(x)=\sum\limits_{n=2}^\infty (n+r)(n+r-1)x^{n+r-2}$
quando aplicado na equação  

$$\begin{align}x^2\sum\limits_{n=2}^\infty a_n(n+r)(n+r-1)x^{n+r-2}+\\ 
2x\sum\limits_{m=1}^\infty a_n (n+r)x^{n+r-1}+\\(x^2-n(n+1))\sum\limits_{n=0}^\infty a_n x^{n+r} =0\end{align}$$
$$\begin{align}\sum\limits_{n=2}^\infty a_n(n+r)(n+r-1)x^{n+r}+\\ 
2\sum\limits_{m=1}^\infty a_n (n+r)x^{n+r}+\\\sum\limits_{n=0}^\infty a_n x^{n+r+2}+\\ -n(n+1)\sum\limits_{n=0}^\infty a_n x^{n+r} =0\end{align}$$
$$\begin{align}\sum\limits_{n=2}^\infty a_n(n+r)(n+r-1)x^{n+r}+\\ 
2\sum\limits_{m=1}^\infty a_n (n+r)x^{n+r}+\\\sum\limits_{n=2}^\infty a_{n-2} x^{n+r}+\\ -n(n+1)\sum\limits_{n=0}^\infty a_n x^{n+r} =0\end{align}$$



Definindo $y=\frac{1}{\sqrt{x}}w(x)$, obtemos $x^2w''+xw'+(x^2-(n+\frac{1}{2})^2)w\Rightarrow \begin{cases}J_{n+\frac{1}{2}}(x)\\ Y_{n+\frac{1}{2}}(x)\end{cases}$
e a solução na variável original é $\begin{cases} j_n(x) = \sqrt{\frac{\pi}{2x}}J_{n=\frac{1}{2}}(x)\\ \eta_n(x)=\sqrt{\frac{\pi}{2x}}Y_{n+\frac{1}{2}}(x) \end{cases}$
