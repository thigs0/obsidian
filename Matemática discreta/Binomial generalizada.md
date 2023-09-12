Dado $u \in \mathbb{R}$ e $r \in \mathbb{N}$ definimos o [[Binomial]] generalizado por:
$\begin{pmatrix} u \\r\end{pmatrix} = \begin{cases} \frac{u.(u-1)(u-2)...(u-r+1)}{r!}~~,r>0\\ 1, ~~r=0\end{cases}$

com essa notação temos
$\displaystyle \large (1+x)^u = \sum_{r=0}^\infty \begin{pmatrix} u\\r\end{pmatrix} x^r$ 

Calculo binomial generalizada
```julia
fuction binom(x, u)
	s=0
	r=0
	while (r>0 && r<10^18)
		ut = 1
		for i in 0:r
			ut *= u-r+1
		end
		ut = ut/(r!)
		s += (u!/( (u-r)!*r!))*x^r
		r+=1
	end
end
```