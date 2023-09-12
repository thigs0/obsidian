Seja $A = (a_{ij})$ uma [[Matriz]] nxn

**Definição**
	A transposta da matriz A, denotada por $A^{t}$, $A^t = (b_{ij})$
**Definição** 
	A é uma [[Matriz simétrica]] se $A=A^T$
**Definição** 
	A é uma  [[Matriz definida positiva]], se A é uma matriz simétrica e satisfaz $\displaystyle x^TAX > 0 ~~\forall x \neq 0,~x \in \mathbb{R}^n$ 

#### Teorema
Se A é definida positiva, então A é não-singular
	Dem: Supomos que A é singular. Então existe $x \in \mathbb{R}^n, x \neq 0~~tal~que~Ax=0$. Dai, $X^TAX=0$,
	Logo, A não é definida positiva.
#### Teorema
Seja $\displaystyle M \in \mathbb{R}^{nxn}$ real, não-singular e $A=M.M^T$. Então A é definida positiva
	Dem: $A = MM^T$=> $A^T =(MM^T)^T= MM^T$ => $A = A^T$ 
	Seja $x\in \mathbb{R}^n~~e~~x\neq 0$
	Então:
	$\displaystyle X^TAX= X^TMM^TX = (M^TX)^T.(M^TX) = ||M^Tx||_2^{2}$, Como M é não singular, o resultado é extritamente positivo


**Exemplo**
$\begin{pmatrix} 2 & -1\\ -1 & 3\end{pmatrix}$ é definida positiva.

#### Teorema
(Decomposição de Cholesky). Seja A uma matriz definida positiva. Então, A pode ser decomposta de uma única forma $$A =GG^T$$
tal que G é uma matriz triangular inferior e tem as entradas da diagonal principal positiva. G é conhecida como [[Fator de Cholensky]]
$\begin{cases} GY=b \\ G^TX=Y\end{cases}$

Vamos enocntrar $GG^T$
$G = \begin{pmatrix} g_{11} & 0 & 0&...&0\\ g_{21} & g_{22} & ...&...&0\\...&...&...&...&...\\ g_{n1} & g_{n2} &...&..&g_{nn} \end{pmatrix}$
Fazendo $GG^T = A$, obtemos o sistema
$\displaystyle \begin{bmatrix} g_{11}^2 & g_{11}g_{21} & g_{11}g_{31}& ...&g_{11}g_{n1}\\ g_{11}g_{21} & g_{21}^2+g_{22}^2 & g_{21}g_{31}+g_{22}g_{32} & ...& g_{21}g_{n1}+g_{22}g_{n2} \\ ...&...&...&...&... \\ g_{n1}g_{11} & g_{n1}g_{21}+g_{n2}g_{22} & g_{n1}g_{31}+g_{n2}g_{32}+g_{n3}g_{33}&...& \sum_{i=1}^n g_{ni}^2\end{bmatrix}$

- Cálculo da 1º coluna de G: Multiplicar a i-ésima linha de G pela primeira coluna de $G^T$ 
=> $g_{i1}g_{11}=a_{i1}$,
para i=1 -> $g_{11}^2 = a_{11}$ -> $a_{11} = \sqrt{a_{11}},~~a_{11}>0$
$\displaystyle g_{i1} = \frac{a_{i1}}{g_{11}}$

- Caĺculo da 2º coluna de G: Multiplicar a i-ésima linha de G com a segunda coluna de $G^T$
$g_{12}=0$
=> $a_{12} =g_{i1}g_{21}+g_{i2}g_{22}$, i=2,...,n
para i=2 => $g_{22}=\sqrt{a_{22}-g_{21}^2}$
para qualquer i=> $\displaystyle g_{i2}=\frac{a_{i2}-g_{i1}g_{21}}{g_{22}}$, i=3,...,n

De forma a termos duas fórmulas para encontrar os valores de G, uma para diagonal e outra para a não diagonal
Agora, se as primeiras (j-1) colunas de G estão calculadas, vamos calcular a j-ésima coluna de G. $$a_{ij}= g_{i1}a_{j1}+g_{i2}g_{j2}+...+a_{ij}g_{jj}$$
para i=j => $a_{jj} = g_{j1}^2+ g_{j2}^2+...+g_{jj}^2$ 
$\displaystyle g_{jj} = \sqrt{a_{jj} - \sum_{k=1}^{j-1}g_{jk}^2}$
Para i=j+1,....,n
$\displaystyle g_{ij} = \frac{a_{ij}-\displaystyle \sum_{k=1}^{j-1}g_{ik}g_{jk}}{g_{jj}}$

O algoritmo que desenvolvemos é conhecido como método de Cholesky

Resolva o sistema 
$$\begin{bmatrix}4 & -2 & 4 &2\\ -2 & 10 & -2 & -7\\ 4& -2 & 8 & 4\\ 2 & -7 & 4 &7\end{bmatrix}\begin{bmatrix}x_1 \\ x_2 \\x_3\\x_4\end{bmatrix} = \begin{bmatrix}8 \\ 2 \\ 16 \\ 6\end{bmatrix}$$
$g_{11} = \sqrt{4}= 2$
$\displaystyle g_{21} = \frac{-2}{2} = -1$
$\displaystyle g_{31} = \frac{4}{2} = 2$
$\displaystyle g_{41} = \frac{2}{2} =1$

$g_{22} = \sqrt{a_{22}-g_{21}^2} = \sqrt{10 - 1}= \sqrt{9}=3$ 
$\displaystyle g_{32}= \frac{a_{32}-g_{31}g_{21}}{g_{22}}= \frac{-2 -2.-1}{3} = 0$ 
$\displaystyle g_{42} = \frac{a_{42}- g_{41}g_{21}}{g_{22}} = \frac{-7 - 1.-1}{3} = -2$   
$\displaystyle g_{43} = \frac{a_{43} - g_{31}g_{41}+g_{32}g_{42}}{g_{33}} = 1$ 

$g_{33} = \sqrt{a_{33} - g_{31}^2-g_{32}^2} = \sqrt{8- 4 - 0}=\sqrt{4}=2$ 
$\displaystyle g_{34} = \frac{a_{34}- g_{31}g_{41} - g_{32}g_{42} - g_{33}g_{43}}{g_{33}} =1$ 


$g_{44} = \sqrt{a_{44} - g_{41}^2 - g_{42}^2 - g_{43}^2}= \sqrt{7 - 1-16/3 - 49}$ 

$\begin{bmatrix} 2 & 0 & 0& 0\\ -1 & 3 &0 &0 \\ 2 & 0 & 2 &0 \\ 1 & -2 & 1 & 1\end{bmatrix}$

**Algoritmo**

**Pseudo-algoritmo**
A <- Matriz definida positiva
G <- matriz de zeros que queremos encontrar
n = Quantidade de linhas em A

G[1, 1] = sqrt(A[1, 1]);
**Para** i de 2 até n
	G[i, 1] = A[i, 1]/G[1, 1]
**Para** i de 2 até n
	**Para** j de 2 até i-1
		G[i, j] = A[i, j]
		**Para** k de 1 até j-1
			G[i, j] = G[i, j] - G[i, k].G[j, k]
		G[i, j] = G[i, j]/G[j ,j]
	#Calcula os termos da diagonal
	G[i, i] = A[i, i]
	**Para** j de 1 até i-1
		G[i, i] = G[i, i] - (G[i, j])^2
	G[i, i] = sqrt(G[i, i])

**Complexidade do algoritmo**


```julia
using LinearAlgebra

function Cholesky(A)
  #= A é a matriz com dimensão nxn que iremos decompor e é definida positiva=#
  
	n,m = size(A);
	
	if n != m
	  error("A matriz não é quadrada")
	end
	
	G = zeros(n,n);
	
	#resolve para a primeira coluna
	G[1,1] = sqrt(A[1,1]);
	for i in 2:n
	  G[i, 1] = A[i, 1]/G[1, 1];
	end
	
	# Itera para as próximas
	for i in 2:n
	  #calcula os outros termos
	  for j in 2:i-1
		G[i,j] = A[i, j];
		for k in 1:j-1
		  G[i, j] -=G[i, k]*G[j, k];
		end
		G[i,j] /= G[j, j]
	  end
	
	  # calcula para a diagonal
	  G[i, i] = A[i,i];
	  for j in 1:i-1
		G[i,i] -= (G[i,j])^2
	  end
	  G[i,i] = sqrt(G[i,i])
	end
	
	return G;
end
```
**Outras formas de se obter os fatores**
- Usada geralmente, com particionamento de matriz
	$A = \begin{bmatrix} a_{11} & b\\ b & \hat A\end{bmatrix} = \begin{bmatrix} g_{11} & 0\\ h & \hat G\end{bmatrix}\cdot \begin{bmatrix} g_{11} & h^T\\ 0&\hat G^T \end{bmatrix}$, observe que h neste caso é um vetor de $\mathbb{R}^{1x(n-1)}$
	=> $\begin{bmatrix} g_{11} & g_{11}h^T \\ g_{11}h & hh^T + \hat G \hat G^T\end{bmatrix}$ => $\begin{cases} a_{11} = g_{11}^2 \\ =h.g_{11} \\ \hat A = h.h^T + \hat G \hat G^T\end{cases}$ 
	-> Reduzimos o problema inicial que era nxn a um problema (n-1)x(n-1), devemos agora encontrar o fator de cholesky para Ã
	Podemos usar o mesmo racioncínio e a cada iteração diminuir de uma unidade a dimensão do problema
	Obs: Este procedimento é conhecido como forma "ouder-product" [[Produto externo]]


