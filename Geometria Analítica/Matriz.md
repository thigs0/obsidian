- Propriedades
	i) A+B = B+A
	ii) A+(B+C) = (A+B)+C
	iii) A+0 =A

- **Multiplicação por escalar**
	A = $[a_{ij}]_{mXn}$ e $K \in \mathbb{R}~~ \forall ~~\mathbb{C}$  
	
	Propriedades
	i) K(A+B) = KA+KB
	ii) ($K_1 +K_2$)A = $K_1 A+K_2A$
	iii) 0.A = 0
	iv) $K_1(K_2A)=(K_1K_2)A$

**[[Matriz Transposta]]**
	Se A = $[a_{ij}]_{mxn}$; $A^t = [b_{ij}]_{nxm}$, tal que $b_{ij} = a_{ji}$. $A^t$ é a transposta de A
	**Propriedades**
	i) Uma [[Matriz simétrica]] atende à apenas se $A=A^t$
	ii) $(A^t)^t = A$
	iii) $(A+B)^t = A^t +B^t$
	iv) $(kA)^t = k(A)^t$

**Multiplicação de matrizes**
	Se $A = [a_{ij}]_{mxn}$ e $B = [b_{ij}]mxn$, definimos A.B = $[c_{ij}]_{mxn}$
	$$c_{ij} = \sum_{k=1}^n a_{ij}b_{ij}+...+a_{in}b_{nj}$$

**Teorema**
	Toda matriz $A_{mxn}$ é linha equivalente a uma única matriz-linha reduzida à forma escada
	Prova:
	Seja A uma matriz $mxn$ qualquer. Se todo elemento da primeira linha é 0, então a condição está satisfeita
	Se a primeira linha tiver um elemento não nulo, multiplicamos a primeira linha por $1/a_{ij}$ e novamente a condição está satisfeita em seguida para elementos $i \geq 2$ somemos ($-a_{jk}$).Por fim, temos de forma que o sistema admite apenas uma solução
$\textbf{Teorema}$ 
a) O [[Sistema linear]] AX=B tem solução única se e somente se A é invertível
	Prova:
	Se A é invertível; 
	$AX=B \Rightarrow A^{-1}(AX)= A^{-1}B$
	$IX = A^{-1}B \Rightarrow X = A^{-1}B$
b) O sistema homogêneo AX=0 apenas se A é invertivel

**[[Determinante]]**

###### [[Matriz de rotação]]
- Preserva a norma dos vetores
- é totalmente determinada sobre a ação sobre $\begin{bmatrix} 1\\0\end{bmatrix}$ e $\begin{bmatrix}0 \\1 \end{bmatrix}$ 
Q = $\begin{bmatrix} cos(\theta) & -sen(\theta)\\ sen(\theta) & cos(\theta)\end{bmatrix}$ 
**Exemplo**
$x = \begin{bmatrix} x_1 \\x_2\end{bmatrix}; x \neq 0$ ; Queremos Q, tal que 
$Q^Tx = \begin{bmatrix} y \\x\end{bmatrix}$ para algum $y \in \mathbb{R}$
escolha $\displaystyle \cos(\theta) = \frac{x_1}{||x||}$ , $\displaystyle sen(\theta) = \frac{x_2}{||x||}$
