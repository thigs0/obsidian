O método de [[Método de Gauss-Seidel]] é bastante atrativo por causa de sua simplicidade. Porém, se o raio espectral de R é muito próximo de 1, então ele pode ser muito lento para convergir. Para contornar este problema, introduzimos a seguinte modificação ao método de Gauss-Seidel
Para i=1:n
$$x^{(k+1)}_{i}= \frac{\omega\left(b_{i}- \displaystyle \sum_{j=1}^{i-1}a_{ij}x_{j^{(k+1)}}- \sum_{j=i+1}^{n}a_{ij}x_j^{(k)}\right)}{a_{ii}}~+~(1-\omega)x_i^{(k)}$$com $\omega \in \mathbb{R}$ 
- $\omega$ é chamado de [[Parâmetro de relaxação]]
- Se $\omega =1$, então o método SOR=gauss-Seidel
- $1 < \omega <2$ Caracteria os métodos de sobre-relaxação
- O método (I) só converge se $0 < \omega< 2$ 
---
**Exemplo**
Ax=b => Sor, $\omega = 1.25$, $x^0=\begin{pmatrix}1 \\ 1 \\ 1\end{pmatrix}$
O sistema $\begin{cases} 4x_{1}+3x_{2}=24 \\3x_{1}+4x_{2}-x_{3}=30 \\-x_{2}+4x_3=-24\end{cases}$, Tem solução $\begin{pmatrix}3 \\ 4 \\ -5\end{pmatrix}$, até $x^7$

**Definição**:
	O [[Raio espectral]] de R é $\rho(R)=\max |\lambda|$ 

**Teorema**
A iteração $x^{(k+1)} = Rx^{(k)}+c$ converge para a solução de Ax=b para todo $x^{(0)}$ e para todos b se e somente se o [[Raio espectral]] for menor que 1, $\rho(R) <1$ 
**Teorema**
Se $A \in \mathbb{R}^{n_{x}n}$ é simétrica e é [[Matriz definida positiva]] então o método de Gauss-Seidel converge para qualquer $x^0$

---
**Algoritmo**
	A <- Matrix que queremos resolver
	x <- vetor inicial
	n <- Dimensão da matrix A
	w <- Parâmetro determinado
	**Para** i de 1 até n
		t = $b_i$
		**Para** j de 1 até i-1
			t -= $a_{ij}x_j$
		**Para** j de i-1 até n
			t -= $a_{ij}x_j$ 
		t /= $a_{ii}$
		t += (1-w)$x_i$ 
		$x_i$ = t
```julia
function SOR(A, b, x,omega=1, max=100)
	n,m = size(A);
	xa = copy(x); #x anterior
	t=0
	if (omega > 2 && omega <0)
		error("O valor atribuido para omega não é válido")
	end
	
	for iter in 1:max
		for i in 1:n
			t = b[i];
			for j in 1:n
				if (j != i)
					t -= A[i, j]*xa[j];
				end
			end
			t /= A[i, i];
			xa[i] = t+(1-omega)*xa[i]
		end
		
	end
	return xa;
end
```