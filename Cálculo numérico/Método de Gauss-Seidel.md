- Método iterativo para [[Sistema linear]]
- Mais rápido que o [[Método de Jacobi]]

$\Large \textbf{Teorema}$ 
	O método iterativos converge com qualquer valor inicial $\large \vec x^0$ se, e somente se, P$(M)$ <1
, onde p$(M)$ é o raio espectral (_maior valor em módulo_)  de M

**Pseudo-algoritmo**
		m <-- Matriz
		v <- Vetor aproximação
		n <- tamanho da matrix quadrada
		Para i de 0 até n 
		v(i) <-- m(linha=i, coluna final)
			Para j de 0 até n+1 # a matriz tem mais colunas
				Se J é diferente de i
					v(i) <-- v(i) - v(j).m(linha=i, coluna=j)
			v(i) <-- v(i)/m(linha=i, coluna=i)
	```
- **Octave**
```octave
function v =GaussSeidel(matrix, aprox)
v = aprox;
m = matrix; # matriz a analisar
n = length(matrix)-1; # armazena o tamnho da linhas
while norm(matrix(:,1:n)*(v)'-matrix(:,n+1),inf) > epsilon # Critério de parada 
for i=1:n #Percorre a linha
	v(i) = matrix(i,n+1); # armazena o valor
	for j=1:n #Percorre a coluna
		if j!=i
		v(i) = v(i)-v(j)*m(i,j); # Subtrai usando as aproximações
		endif
	endfor
	v(i) = v(i)/m(i,i);
endfor
endwhile
endfunction
```
**[[Julia]]**
```julia
using LinearAlgebra

function GaussSeidel(A, b, x, max=100)
	n,m = size(A);
	xa = copy(x); #x anterior
	for iter in 1:max
	
		for i in 1:n
			xa[i] = b[i];
			for j in 1:n
				if (j != i)
					xa[i] -= A[i, j]*xa[j];
				end
			end
			xa[i] /= A[i, i];
		end
	end
	return xa;
end
```
**Python**
```python
def GaussSeidel(m, aprox)
import numpy as np
	v = np.array(aprox)
	m = m
	n = len(matrix) # armazena o tamanho das linhas
	while np.norm(m*aprox) < lembda:
		for i in range(1,n):
			for j in range(1,n):
				if i != j: # ignoramos o termo da diagonal
					aprox[i] = aprox[i] - aprox[j]*m[i,j]
		aprox[i] = aprox[i]/m[i,i] #Dividimos pelo termo da diagonal
	return aprox
```
```mathematica
function 
```

_Exemplo_
$\begin{cases} 2x_1 - x_2=2\\ x_1+2x_2=11\end{cases}$
Iteração 1: $\large \begin{cases} x_1^1 = \frac{1}{2}(2+0)=1\\ x_2^1 = \frac{1}{2} (11-1)=5\end{cases}$
Iteração 2:  $\large \begin{cases} x_1^2 = \frac{2+x_2^1}{2} = \frac{7}{2}\\ x_2^2 = \frac{11-x_1^2}{2} = \frac{15}{4}\end{cases}$

$\Large \textbf{Teorema}$:
	O [[Critério das linhas]] também é condição suficiente para o método de Gauss-Seidel
	&
	[[Critério de Sassenfeld]]

$\large \textbf{Teorema}$ ([[Critério de Sassenfeld]])
	Considere o sstema linear dado por Ax=b e defina os coeficientes 
	$\large \beta_1 = \frac{1}{|a_{11}|}(|a_{12}|+|a_{13}|+|a_{14}|+...+|a_{1n}|)$ = $\alpha_1$
	$\large \beta_j = \frac{1}{|a_{jj}|}(|a_{j1}|\beta_1+|a_{j2}|\beta_2+|a_{j3}|\beta_3+...+|a_{jj^{-1}}|\beta_{j-1}+|a_{jj+1}|+...+|a_{jn}|)$ = $\alpha_i . \beta_i^T$
	Se $\beta = \max-{1\leq i \leq n} \beta_i <1$, então o método do Gauss-Seidel gera uma sequência convergente para a solução do sistema dado, independentemente da escolha da aproximação inicial $\vec x^0$
	 **Obs**
	 Quanto menor o valor de $\beta$, mais rápido o sistema irá convergir
	_Exemplo_
		Teste o sitema abaixo pelos dois critérios acima e veja se ele converge para gauss-seidel e gauss-jacobi:
		$$\begin{cases} +2x_1+0.5x_2-0.1x_3+0.1x_4=0.2\\ +1x_1+ x_2-0.2x_3-0.1x_4=-2.6
	\\-0.1x_1-0.2x_2+x_3+0.2x_4=10\\ +0.1x_1+0.3x_2+0.2x_3+x_4=-2.5\end{cases}$$
		**a) critério das linhas**
		$\alpha_1 = \frac{0.5+0.1+0.1}{2}= 0.35$
		$\alpha_2= \frac{1+0.2+0.1}{1}= 1.3$, falhou
		**b) Critério de Sassenfeld***
		$\beta_1 = \frac{0.5+0.1+0.1}{2}= 0.35$
		$\beta_2 = \frac{1_x0.35+0.2+0.1}{1} = 0.65$
		$\beta_3 = \frac{0.1_x0.35+0.2_x0.65+0.2}{1}= 0.365$
		$\beta_4 = \frac{0.1_x0.35+0.3_x0.65+0.2_x0.365}{1}=0.363$
		por este método, ele converge para Seidel
		para jacobi, é inconclusivo

==Qual a matriz M do método de Gauss-Seidel?==
	Consideremos o sistema linear Ax=b e escrevamos novamente $$A=D+E+F$$
	de forma $\begin{bmatrix} a_{11}x_1 + a_{12}x_2 +a_{31}x_3+...+a_{1n}x_n \\a_{21}x_1+ a_{22}x_2 + a_{32}x_3+...+a_{2n}x_n\\ ...\\ a_{n1}x_1+a_{n2}x_2+a_{n3}x_3+...+a_{nn}x_n \end{bmatrix} = D + E + F$
	Então: $(D+E+F)x=b \Rightarrow (D+E)x = -Fx+b \Rightarrow x=-(D+C^{-1}Fx + (D+E)^{-1})b$,  e assim temos que o método também é de ponto fixo 