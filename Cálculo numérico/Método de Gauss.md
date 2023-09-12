- Resolução de sistemas matriciais
	- [[Operações elementares]]
	- Eliminação gaussiana
	- [[Escalonamento]]

- ### Caso simples:  Sistema triângular
	$$\begin{bmatrix} a_{11} & a_{12} &...& a_{1n-1} & a_{1n}\\ 0 & a_{22} &...& a_{2n-1} & a_{2n} \\
	0 & 0& ...& a_{n-1n-1} & a_{n-1n}\\ 0 & 0 &...& 0 & a_{nn}\end{bmatrix}$$
	- Algoritmo
	```octave
function m=triangular(matrix)
	[i,j] = size(matrix);
	if i!=j-1;
		error('A matrix não é quadrada')
	endif
	n=i;m=1:n;
	m(end)= matrix(end, end)/matrix(end,end-1);
	for i=n-1:-1:1 # da última linha até a primeira
		s=0;
		for j=i+1:1:n
			display(matrix(i,j))
			display(j) 
			s+= matrix(i,j)*m(j);
		endfor
		m(i) = (matrix(i, end)-s)/matrix(i,i);
	endfor
endfunction
	```

**Algorítmo**
	- **Pseudo-código**
		Para j=1:n-1
			Para i=j+1:n
				m = $a_{ij}/a_{jj}$, Se $a_{jj} \neq 0$ 
				Para k=j:n+1
				$a_{ij}$ <-- $-ma_{jk}+a_{ik}$
	- **Octave**
```octave
#Código escalonamento de gauss-jordan
Matrix = [1 2 1 2; 2 1 1 2; 1 1 2 2];
function Matrix = matriz(A)
%#Resolve por eliminação gausiana para triangularizar uma matriz
%#
Matrix = A;
n = size(Matrix)(1);
linha_temp = 1;

# Fixa uma linha e zero tudo abaixo
for linha_loop=1:n
  for linha= linha_loop+1:n
    # troca a linha
    if (Matrix(linha_temp,linha_temp) == 0)
    aux = Matriz(linha_temp);
    Matriz(linha_temp) = Matriz(n);
    Matriz(n) = aux;
    endif
    m = Matrix(linha,linha_temp)/Matrix(linha_temp,linha_temp);
    
    #percorre as colunas mudando
    for coluna=linha_temp:n+1
    Matrix(linha, coluna) = Matrix(linha, coluna) - m*Matrix(linha_temp,coluna);
    endfor
	endfor
  linha_temp= linha_temp+1;
endfor
endfunction
```

```octave
function A=lugauss(A)
[n,m] = size(A)
if n == m
error("A não é uma matriz quadrada")
else
for k = i:n-1
	for i = k+1>n
	A(i,k) = A(i,k)/A(k,k)
	if a(k,k) == 0
	error("Elemento diagonal nulo")
	endif
	j = [k+1:n];
	A(i,j) = A(i,j) - A(i,j)*A(k,j)
	endfor
	endfor
endif
endfunction
```


## Decomposição LU
- Podemos usar o método de gauss para contruir um método de decomposição da matriz M, em uma L inferior e uma U superior

$M = \begin{bmatrix} a_1 & a_2 & a_3 & ... & a_n \\ a_1 & a_2 & a_3 & ... & a_n \\ ... & ... & ... & ... & ... \\ a_1 & a_2 & a_3 & ... & a_n \end{bmatrix}$ ; $U =  \begin{bmatrix} a_1 & a_2 & a_3 & ... & a_n \\ 0 & a_2 & a_3 & ... & a_n \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & a_n \end{bmatrix}$ e $L =  \begin{bmatrix} a_1 & 0 & 0 & ... & 0 \\ a_1 & a_2 & 0 & ... & 0 \\ ... & ... & ... & ... & ... \\ a_1 & a_2 & a_3 & ... & a_n \end{bmatrix}$
Normalmente $U$  sai da decomposição pelo método de Gauss
M = LU

A vantagem vêm de podermos realizar as operações para a mesma matrix A com um custo das segundas para a frente de $\displaystyle n^2$ para cada uma 

$\displaystyle Ax = B \Rightarrow LUx = B$; podemos decompor em dois sistemas

$\begin{cases} Ly = b \\ Ux = y\end{cases}$ ; Este sistema é simples de se revolver por tratar de matrizes triangulares

Quando tivermos que fazer a fatoração com pivoteamento teremos $PA= LU$ e precisamos preparar o vetor b para a a solução
$$Ax = b \Rightarrow PAx= Pb \Rightarrow LUx=Pb \Rightarrow  \begin{cases} Ly=pb \\ Ux =  y\end{cases}$$
- Aplicação: Cálculo do determinante
	$\det A = \det L. \det U$
	Mas -> $\det L = \det \begin{bmatrix} 1 & ...& 0\\ 0 & 1 ...& 0\\ algo & ...& 1\end{bmatrix} =1$ **e** $\det U = \det \begin{bmatrix} u_{11} & ...& 0\\ algo & u_{ii} ...& 0\\ algo & ...& u_{nn}\end{bmatrix} = u_{11}u_{22}u_{33}...u_{nn}$

$\Large \textbf{Teorema}$
	Seja A uma matrix nxn e $A_k$ a submatriz principal de ordem k. Se $\det A_k \neq 0~~; ~~ k= 1,2,...,n$
	então existe úninca matriz triangular interior L com $l_{ii} = 1, i=1,2,3,...n$ e uma única matriz triangular superior U tais que $A=LU$
- _Casos expeciais_
1. A= LU pode ser escrita como $A =LD\bar U$, de forma que D é diagonal e $\bar U$  tem a i-ésima $u_{in}$linha é a i-ésima linha de U dividida por $U_{in}$
 $$\bar U =  \begin{bmatrix} a_1 & a_2 & a_3 & ... & a_n \\ 0 & a_2 & a_3 & ... & a_n \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & a_n \end{bmatrix}.\begin{bmatrix} \frac{1}{a_1} & 0 &...&0 &0 \\ 0 & \frac{1}{a_2} & ... & 0 &0\\ ...& ... &...& ...&...\\0 & 0 &...&0& \frac{1}{a_n}\end{bmatrix}=UK$$
 Consideramos o caso em que A é simétrica, isto é, $A^T =A$ então:
 $\displaystyle A = A^t = (LD\bar U)^t =\bar U^{-t} D^t l^t = \bar u^{-t}DL^t \Rightarrow LD \bar U = \bar U^t DL^t$; tal que $\bar U$ é triangular inferior com 1 na diagonaise $L^t$ triangular superior com 1 na diagonal
 
 Caso A seja uma [[Matrix simétrica]] e seja também uma [[Matrix definida positiva]] temos que $\displaystyle d_{ii} >0~~\forall i$
 com isso, podemos escrever $D= \bar {DD}$, com $\bar D = \begin{bmatrix} \sqrt{d_{11}} & ...& 0\\ 0 & \sqrt{d_{22}} & 0\\ 0 & ...& \sqrt{d_{nn}}\end{bmatrix}$
 Logo, $\displaystyle A  = L \bar D \bar D L^t = (L \bar D) (L \bar D)^t$ (D é simétrica).   
 
 $\Large \textbf{Teorema}$  : [[Fatoração de Cholensky]]
	 Se A é matrix $\displaystyle n_xn$ é  simétrica e positiva definida então existe uma única matriz triangular interior com diagonal positiva G, tal que $$A = GG^t$$
	 - _Exemplo_
		 Ache, se existir, a fatoração de cholensky para a matriz
		 $\displaystyle A = \begin{bmatrix} 9 & 3 & 3\\ 3 &10& 5 \\ 3 &5&9\end{bmatrix}$ queremos G triangular inferior e $A=GG^t$
		$$\displaystyle \begin{bmatrix} g_{11}^2 & g_{11}g_{21} & g_{31}g_{11}\\ g_{21}g_{11} & g_{22}^2+ g_{21}^2 & g_{21}g_{31}+g_{22}g_{32} \\ g_{31}g_{11} &g_{31}g_{21}+g_{32}g_{22} & g_{31}^2+g_{32}^2+g_{33}^2  \end{bmatrix}=\begin{bmatrix} 9 & 3 & 3\\ 3 &10& 5 \\ 3 &5&9\end{bmatrix}$$
		Este código tem complexidade de $\frac{1}{3}n^3$
		e G = $\begin{bmatrix} 3 & 0 &0 \\ 1 &3 & 0\\ 1 & \frac{4}{3} & \frac{2\sqrt{14}}{3}\end{bmatrix}$
		
 

#### Algoritmo para decomposição LU
- Pseudo algoritmo
	U <--  A ; L<-- I
	Para j = 1,2,... n-1
		Se $u_{jj}=0$ , então A não tem decomposição LU
		Para i = j+1, j+2, ... , n
			$\displaystyle l_{ij}$ <-- $\displaystyle \frac{u_{ij}}{u_{jj}}$
			$u_{ij}$ <-- 0
			Para k = J+1, ..., n
				$u_{ij}$ <-- $u_{ij}-l_{ij}u_{jk}$

- Octave
	```octave
	function [L,U] = LU(matrix)
	n = length(matrix) # Dimensão da matriz quadrada
	L = eye(n)
	for j = 1:n
		if matrix(j,j) == 0
			error("Não há decomposição para esta matriz")
			# escrever troca de linhas
			
		endif
		for i = j+1:n
			L(i,j) = matrix(i,j)/matrix(j,j) # multiplicador
			matrix(i,j) = 0
			for k = j+1:n
			matrix(i,k) = matrix(i,k)-L(i,j)*matrix(j,k) # atualiza a linha da matrix
			endfor
		endfor
	endfor
	U = matrix
	endfunction
	
	```
	```julia
	function LU(matrix)
	using LinearAlgebra
	
	n = length(matrix) # Dimensão da matriz quadrada
	L = matrix{Float64}(I, n, n) #Cria matrix identidade com a biblioteca LinearAlgebra
	for j in 1:n-1
		if matrix[j,j] == 0
			println("Não há decomposição para esta matriz")
			break 
		end
		for i in j+1:n
			L[i,j] = matrix[i,j]/matrix[j,j]  # Multiplicador
			matrix[i,j] = 0
			for k in j+1:n
				matrix[i,k] = matrix[i,k]-L[i,j]*matrix[j,k] # Atualiza a linha da matrix
			end
		end
	end
	U = matrix
	return [L,U]
			 
	```


- **Custo operacional**
É calculado usando [[Somatória de Gauss]]
Transformando as operaçẽos, temos: $\displaystyle \sum_{j=1}^{n-1}\sum_{i=j+1}^n [1+2(n-j)]$  que é  $\displaystyle \frac{2}{3} n^3 ~flops$ 
