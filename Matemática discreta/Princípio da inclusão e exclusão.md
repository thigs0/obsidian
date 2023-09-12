Dado dois conjuntos A e B. temos:
$$|A\cup B|=|A|+|B|-|A \cap B|$$
De forma generalizada
$$|\cup_{i=1}^{n} A_i| = \sum_{i=1}^n|A_i|-\sum_{1 \leq i\leq j\leq n} |A_i\cap A_j|+\sum_{1 \leq i\leq j\leq k\leq n} |A_i\cap A_j\cap A_k|+...+(-1)^{n-1}|A_1 \cap ...\cap A_n|$$
**Prova**:
	Considere $x \in U_{i=1}^n A_i$ , digamos que ele pertence a p conjuntos =>
	(I) x está sendo contado p vezes
	(II) x está sendo contado $\begin{pmatrix}P\\2\end{pmatrix}$ vezes. Pois, há $\begin{pmatrix}P\\2\end{pmatrix}$ formas 
	...
	...
	...
	P - $P-\begin{pmatrix}P\\2\end{pmatrix}+\begin{pmatrix}P\\3\end{pmatrix}-\begin{pmatrix}P\\4\end{pmatrix}+...+(-1)^{p-1}\begin{pmatrix}P\\P\end{pmatrix}$ 
	= $\displaystyle \left[ \sum_{k=0}^p 1.(-1)^k.\begin{pmatrix}P K\end{pmatrix}\right](-1)+\begin{pmatrix}P\\0\end{pmatrix} = ((-1)+1)^p+\frac{P!}{0!P!}=1$


[[Função de Euler]]
	Dado um número $m \in \mathbb{N}^*$, chamamos de função $\phi$ de Euler
	$\phi: \mathbb{N}^* \rightarrow \mathbb{N}^*$
	$\phi(m) = |\{1 \leq x \leq m~:~mds(x,m)=1\}|$

**Teorema**
	Seja $m=P_1^{\alpha_1} P_2^{\alpha_2}...P_r^{\alpha_r}$
	$\phi(m) = m\left(1-\frac{1}{P_1}\right)\left(1-\frac{1}{P_2}\right)...\left(1-\frac{1}{P_r}\right)$
	