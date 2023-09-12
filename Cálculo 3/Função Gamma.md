Ela é definida usando [[Integral imprópria]] na forma $$\large \Gamma (x) = \int_{0}^\infty e^{-t}t^{x-1}dt$$
- Propriedades:
	- A função tem a propriedade de ser [[Recursiva]]
		**Exemplo:** vamos calcular para x+1
		$\displaystyle \Gamma (x+1) = \int_{0}^\infty e^{-t}t^{x}dt$, Fazendo a integração por partes $\begin{cases} u = t^x \\ e^{-t}dt\\ du = x t^{x-1}dt\\ v = -e^{-t}\end{cases}$ 
		= $\displaystyle \large -e^{-t}t^x |_0^\infty + \int_{0}^{\infty} xt^{x-1}e^{-t}dt= z\int_{0}^\infty e^{-t}t^{x-1}dt= x \Gamma (x)$ 
	- A função gamma nos reais define o [[Fatorial]],
		$\displaystyle \large \Gamma (1)= \int_0^\infty e^{-t}t^0dt= -e^{-t}|_0^\infty = \lim_{b \to \infty} =-e^{-b}+1=1$
		$\Gamma (2)= x\Gamma (x)= 1\Gamma (1)=1$
		$\Gamma (3) = x\Gamma (x) = 2 \Gamma (2)=2.1$
		$\Gamma (4) = x\Gamma (x) = 3 \Gamma (3)=3.2.1$
		$\Gamma (5) = x\Gamma (x) = 4 \Gamma (4)=4.3.2.1$
		...
		$\Gamma (n+1) = n\Gamma (n) = n \Gamma (n)=n!$