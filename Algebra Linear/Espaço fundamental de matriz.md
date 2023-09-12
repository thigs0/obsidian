A = $\begin{bmatrix} a_{11}\\ a_{21} \\ a_{311}\\...\\ a_{n1}\end{bmatrix} \in \mathbb{R}^{n_xn}$ 
- [[Espaço gerado]] pelos vetores linha da chamamos de [[Espaço linha]] de $A \subset \mathbb{R}^n$ 
- Espaço gerado pelos vetores coluna, chamamos de [[Espaço coluna]] de $A \subset \mathbb{R}^n$
- Um terceiro subespaço importante é $\{x| Ax=0\}$, espaço nulo de A
$A = \begin{bmatrix} a_{11} & a_{12} & ... & a_{1n}\\ a_{21} & ... &...& a_{2n}\\ ... & ...& ...&...\\ a_{n1} & ...&...& a_{nn}\end{bmatrix}\begin{bmatrix} x_1\\x_2 \\...\\ x_n\end{bmatrix}$ = $x_1 \begin{bmatrix} a_{11}\\ a_{21}\\ ...\\ a_{n1}\end{bmatrix}$ + $x_2\begin{bmatrix} a_{12}\\ a_{22}\\ ...\\ a_{n2}\end{bmatrix}$ +...+ $x_n \begin{bmatrix}a_{1n}\\ a_{2n}\\...\\ a_{nn} \end{bmatrix}$ 
combinação linear de colunas

**Teorema**
	O sistema Ax=b tem solução se, e somente se, $b \in$ espaço coluna de A

**Teorema**
	Se $\bar X$ é solução de Ax=b, então todas as outras soluções de Ax=b podem ser escritas como $\bar x +v, v \in nulo(A)$ reciprocamente, todo vetor nessa forma é solução de Ax=b
	Prova
	Seja $x'$ solução de Ax=b. Defina v= $x'-\bar x$
	$A_v = A(x'-\bar x) = Ax' -A\bar x = b-b =0$
	Além  disso, dado $v \in nulo(A)$, $A(\bar x +v) = \bar {Ax} +AV =b$ 

**Teorema**
	As operações elementares usados no [[Escalonamento]] preservam o espaço nulo de uma [[Geometria Analítica/Matriz]] A

**Teorema**
	- As operações elementares preservam o espaço linha
	- As linhas de A' são combinação lineares das linhas originais de A -> ger linhas de A $nsubset$ ger linhas A'

**Teorema**
	Se A e A' são equivalentes por linha, então

a)  um conjunto de vetores coluna de A é LI <-> 0
b) Um conjunto de vetores coluna de A formam uma base do espaço coluna de A <-> 0. Conjunto de coluna de A' formam base do espaço coluna de A'

$\begin{bmatrix} 1 & -3 & 4 & -2& 5&4\\ 2& -6& 9& -1& 8&2 \\ 2&-6&9&-1&9&7 \\ -1&3&-4&2&-5&-4\end{bmatrix} \xrightarrow {\text{Escalonamento}} \begin{bmatrix} 1&-3&4&-2&5&4 \\ 0&0&1&3&-2&-6 \\ 0&0&0&0&1&5 \\ 0&0&0&0&0&0\end{bmatrix}$   
Base linha A = $\{(1,-3,4,-2,5,4),(0,0,1,3,-2,-6),..., (0,0,0,0,0,0)\}$
Base coluna A = $\{(1,2,2,-1), (4,9,9,-4),(5,8,9,-5)\}$

**Dado a matriz** $A \in \mathbb{R}^{m_xn}$
- Espaço linha A = Espaço coluna $A^T \subset \mathbb{R}^n$
- Espaço coluna A = Espaço linha $A^T \subset \mathbb{R}^n$
- Nulo $A \subset \mathbb{R}^n$ nulo($A^T$)$\subset \mathbb{R}^n$
	- Nulidade de A é o nº de linhas na matriz escalonada
	- Posto de A é número de elementos em uma dimensão

**Teorema**
	Se A tem n colunas posto(A) + nulidade = n
	
Corolários
- [[Posto]](A) = Posto($A^T$)
- Posto(A) $\leq min(m,n)$ 