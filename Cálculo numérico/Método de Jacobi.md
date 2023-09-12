Dado um sistema $\large n_xn$ 
$$\begin{matrix} \textcolor{red}{a_{11}}x_1 + a_{12}x_2 +a_{31}x_3+...+a_{1n}x_n = b_1\\
a_{21}x_1+ \textcolor{red}{a_{22}}x_2 + a_{32}x_3+...+a_{2n}x_n = b_2\\
...\\
a_{n1}x_1+a_{n2}x_2+a_{n3}x_3+...+\textcolor{red}{a_{nn}}x_n = b_n\end{matrix}$$
isolamos os termos da diagonal, destacados em vermelho,de modo que:
$\displaystyle a_{ii}x_i = b_i - \left( \sum_{j=1}^{i-1}a_{ij}x_j+ \sum_{j=i+1}^{n}a_{ij}x_j \right)$
e podemos
$\displaystyle x_i = \frac{b_i - \left( \sum_{j=1}^{i-1}a_{ij}x_j+ \sum_{j=i+1}^{n}a_{ij}x_j \right)}{a_{ii}}$
- _Exemplo_
	Resolva o sistema $\begin{cases} 2x_1 - x_2 = 2\\ x_1 +2x_2 =11\end{cases}$
	Passamos para o formato adequado
	$\displaystyle \begin{cases} x_{1}^{k+1} = \frac{2+x_2}{2}\\ x_{2}^{k+1} = \frac{11-x_1}{2}\end{cases}$
	
	Temos o chute inicial $x_0 = (0,~0)$
	obtemos $x_1 = (1, ~11/2)$
	$x_2 = (15/4 ,~5 )$
	$x_3 = (7/2,~ 29/8)$
	$x_4 = (48/16,~ 18/4)$
	$x_5 = (23/8,~ 131/32) \approx (2.875,~ 4.0937)$

**Pseudo-algoritmo**
A <- Matriz de resolução
x <- codição inicial
b <- vetor do sistema
**Para** 1 até n
	**Para** i de 1 até n
		xn[i] <- b[i]
		**Para** j de 1 até n
			**if** j != i
				xn[j] <- xn[j] - A[i, j].x[j]
		xn[i] = xn[i]/A[i, i]
	x <- xn

Tempo de execução:
	Pelo pseudo-algoritmo temos que, cada Para viram uma somatória. Dentro do primeiro escopo não termo operações solitária, no segundo temos uma operação de divisão e no terceiro temos duas operações
	$\displaystyle \sum_{1}^{n} \sum_{i=1}^{n} \left( \sum_{j=1}^{n-1} 2\right)+1 = \sum_{1}^{n} \sum_{i=1}^{n}\left( 2n -2\right)+1= \sum_{1}^{n} \sum_{i=1}^{n}\left( 2n-1\right)= \sum_{1}^{n} n(n+1) -n$ 
	= $\displaystyle \sum_{1}^n n^2+n-n = \frac{n(2n+1)(n+1)}{6} = \frac{1}{3}n^3 + \frac{1}{6}n^2+\frac{1}{3}n + \frac{1}{6}$   
	Então a complexidade do algoritmo é 1/3 de $n^3$ no pior caso
	
```julia
function Jacobi(A, b, x, max=1)
	n,m = size(A);
	xa = copy(x); #x anterior
	xn = Vector{Float64}(1:n); #x novo
	for iter in 1:max
	
		for i in 1:n
			xn[i] = b[i];
			for j in 1:n
				if (j != i)
					xn[i] -= A[i, j]*xa[j];
				end
			end
			xn[i] /= A[i, i];
		end
		xa = xn;
	end
	return xn;
end
```

Qual a matriz do método de jacobi
	consideramos o sitema linear $Ax=b$
	A = $\begin{bmatrix} a_{11}x_1 + a_{12}x_2 +a_{31}x_3+...+a_{1n}x_n \\a_{21}x_1+ a_{22}x_2 + a_{32}x_3+...+a_{2n}x_n\\ ...\\ a_{n1}x_1+a_{n2}x_2+a_{n3}x_3+...+a_{nn}x_n \end{bmatrix} = D + E + F$, de forma que D é diagonal, E triangular inferior e F triangular superior
	Temos $Ax=b \Rightarrow (D+E+F)x=b \Rightarrow Dx = b-(E+F)x \Rightarrow x=D^{-1}(E+F)x+D^{-1}b \Rightarrow x= Mx+C$
	De modo que $x_n = Mx_{n-1}+C$

**Teorema**
Se $\displaystyle \|M\| = \max \frac{\|Mx\|}{\|x\|}$ e $\|M\| <1$, então a fórmula cpnverge para qualquer $x^{(0)}$
Dem:
Seja x a solução do problema Ax=b => (x = Mx+c)
Então subtraindo x = Mx+c de $x^{(k+1)} = Mx^{(k)}+c$, temos $x^{(K+1)} - x = M(x^{(K)}-x)$. Portanto
$\|x^{(K+1)}-x\| = \|M(x^{(K)}-x)\| \leq \|M \|\|X^{(K)}-x\| \leq \|M\|^{2}\|x^{(K+1)}-x\|\leq...\leq\|M\|^{K+1}\|x^{(0)}-x\|$

---
[[Critério das linhas]]
	Considere o sitema linear Ax=b e defina os coeficientes como:
	$$\alpha_i = \frac{1}{|a_{ii}|}\sum_{j=1 j \neq i}^{n} |a_{ij}|$$
	Se $\displaystyle \alpha = \max_{1 \leq i \leq n} \alpha_i <1$; então o [[Método de Jacobi]] gera uma sequência que converge para a a solução do sistema dado, independentemente da escolha aproximação inicial $\vec x^0$
	 **Demonstração**: Cada componente de $\vec x^*$ satisfaz
	 $$\displaystyle x_i^* = \frac{b_i - \left( \sum_{j=1, j \neq i}^{n}a_{ij}x_j^* \right)}{a_{ii}}$$
	 em quanto o método nos dá
	 $$\displaystyle x_i^{k+1} = \frac{b_i - \left(  \sum_{j=1, j \neq i}^{n}a_{ij}x_j^k \right)}{a_{ii}}$$
	 Assim:
	 $\displaystyle |x_i^{K+1}-x_i^*| = \left| \sum_{j=1, j \neq i}^{n} \frac{a_{ij}}{a_{ii}}(x_j^k - x_j^*)  \right| \leq \sum_{j=1, j \neq i}^{n} |\frac{a_{ij}}{a_{ii}}|.|x_j^k-x_j^*| \leq \sum_{j=1, j \neq i}^{n} |\frac{a_{ij}}{a_{ii}}|.\max |x_j^k - x_j^*|$
	 Finalizamos 
	 $\displaystyle |x_i^{K+1} | \leq \alpha_i |\vec x^k - \vec x^*|_\infty \leq \alpha |\vec x^k - \vec x^*|_\infty \Rightarrow |x_i^{K+1} |_\infty \leq \max_{1 \leq i \leq n }{|x_i^{K+1}-x_i^k|} \leq \alpha |\vec x^k - \vec x^*|_\infty$
	 Assim:
	 $$|\vec x^{k+1} - \vec x^*|_\infty \leq \alpha ||\vec x^k -\vec x^*||_\infty$$
	 Se $\alpha$ for menor que 1, quando tomamos o limite, o sistema tende para 0
 
$\Large \textbf{Algoritmo para o critério das linhas}$
	 
- **Pseudo-algoritmo**
	m <- matrix quadrada
	n <- tamanho da matrix
	Para 
	
	
	
```octave
function m = criterio_linahs(m)
	n= length(m);
	for i = 0:n #percorre as linhas
		s=0;
		for j = 0:n # percorre as coluna
			if i !=0
				s += m(i,j); #Soma os elementos da linha menos da diagonal
			endif
		endfor
		
		s = s/m(i,i);
		if s < 0
		error "O método não têm convergência garantida"
		endif
	endfor
	m=1
endfunction
```
```julia
function criterio_linhas(m)
	n = length(m);
	for i in 0:n
		if i !=0
		
```
```octave
function f = GaussJacobi(m, aprox)
	
```
