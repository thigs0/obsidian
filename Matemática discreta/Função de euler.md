Dado um número $m \in \mathbb{N}^*$, chamamos de função $\phi$ de Euler
$\begin{matrix} \phi: \mathbb{N} \rightarrow \mathbb{N}^*\\ \phi (m) = |\{ 1 \leq x \leq m : mdc(x,m)=1\}|\end{matrix}$
- Essa função retorna a quantidade de [[Número primo]]s menores ou iguais a X co-primos 

**Exemplo**
$\phi(1) = (mdc(1)) = 0$ 
$\phi (2) = (mdc(2),~mdc(1)) = (2,1) = 1$ 
$\phi (3) = (mdc(3),~mdc(2),~mdc(1)) = 2$
$\phi (4)= (mdc(4),~mdc(3),~mdc(2),~mdc(1)) =(4,1,2,1)=(2)$
$\phi (5) = (mdc(5),~mdc(4),~mdc(3),~mdc(2),~mdc(1)) = (5,1,1,1,1)=4$
$\phi (6) = (mdc(6),~mdc(5),~mdc(4),~mdc(3),~mdc(2),~mdc(1)) = (6,1,2,3,2,1)=2$ 
...
...
...
$\phi (n) = \# \{ mdc(n,i),~~ i=1,2,3,4,...,n\}$   

**Teorema**
Seja $m = P_1^{\alpha_1} P_2^{\alpha_2}...P_{r}^{\alpha_r}$ em que cada $P_i$ é um primo
$\displaystyle \large \phi (m) = m\left( 1-\frac{1}{P_1}\right)\left( 1-\frac{1}{P_2}\right)...\left(1-\frac{1}{P_r}\right)$
Prova:
	$\displaystyle m= \prod_{i=1}^r \left( P_i^{\alpha_i}\right)$ 
	

**Teorema**
Seja P um número primo maior do que 1. Então, $\phi (P) = P-1$ 
Prova:
	$\phi(P) = \#(mdc(P,i), ~i=1,2,3,...P)$ Como P é primo, o mdc(P,n) para qualquer $n \neq P$ é 1. Então
	$\# (\underbrace{1,1,1,1,...,1}_{P-1},P) = P-1$

```julia
	function Euler_function(m)
		function mdc(m, n)
			k2=1
			maior = min(m,n)
			for i in 2:maior
				if (m%i ==0 && n%i==0)
					k2 =i
				end
			end
			return k2;
		end
		
		k=1;
		for i in 2:m
			if (mdc(m, i) == 1)
				k=k+1;
			end
		end
		return k;
	end

```
