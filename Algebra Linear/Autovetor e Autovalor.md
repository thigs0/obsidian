#### Definição 1
Se A for uma matriz $n\times n$, então um [[Vetor]] não nulo $\vec x$ em $R^n$  é denominado autovetor de A (ou do operador matricial T(A)  se Ax for um múltiplo escalar de
x, isto é: $$A \vec x = \lambda \vec x$$
Em que $\lambda$ é um número real, ele é denominado autovalor de A.

- No caso de um [[Autovetor]], a direção do vetor $\vec x$, não é alterado.

Da definição, podemos multiplicar $\vec x$ pela identidade sem alterá-la $\displaystyle A x = \lambda x \Rightarrow Ax = \lambda Ix \Rightarrow (\lambda I - A)x = 0$

#### Teorema
Se A for uma [[Matriz]] $n \times n$, então $\lambda$ é um [[Autovalor]] de A se, e só se, $\lambda$ satisfaz a equação:
$$det(\lambda I- A)=0$$
Este determinante costuma ser expandido e se mostrar um polinômio de grau $n$, o que pode complicar encontrar a raiz.

#### Teorema
Se A for uma matriz $n \times n$ triangular (superior, inferior, ou diagonal), então os autovalores de A são as entradas na diagonal principal de A.
Exemplo:
$$\det \begin{pmatrix}\\
\lambda-a_{11} &1&3\\
0 & \lambda -a_{22} & 3\\
0 & 0 & \lambda -a_{33}
\end{pmatrix} = (\lambda-a_{11})(\lambda -a_{22})(\lambda -a_{33})=0$$
Podemos observar que neste mesmo caso os valores da diagonal de a são os autovalores.

- ##### Corolário ->
	A matriz quadrada é inversível <=> $\lambda =0$ não é auto valor de A

```octave
M = matrix
eig(M) #Retorna os auto valores em lista
```

# Auto espaço
O autoespaço de A associado ao autovalor $\lambda$ é o espaço solução do sistema homogêneo
$det(\lambda I- A)=0$.

- # Diagonalização
	### Definição ---> Se A e B forem matrizes quadradas, dizemos que B é semelhante a A se existir alguma matriz invertível P tal que $B =P^{-1}AP$ 

	Se uma matriz A é semelhante a B, elas têm o mesmo determinante
		--> prova:
			$\displaystyle det(A) = det(P^{-1}BP) = \frac{1}{det(P^{-1})}det(A)det(B) = det(A)$

##### Definição:
Uma matriz quadrada A é dita diagonalizável se for semelhante a alguma [[Matriz diagonal]], ou seja, se existir alguma matriz invertível P tal que $P^{-1}AP$ é diagonal. Nesse caso, dizemos que a matriz P diagonaliza A.

- ### Algoritmo de diagonalização de uma matriz
	1. Confirme que a matriz é realmente diagonalizável encontrando n autovetores [[Linear independente]]. Uma maneira de fazer isso é encontrar uma base de cada [[Autoespaço]] e juntar todos esses vetores num único conjunto S. Se esse conjunto tiver menos do que n elementos, a matriz não é diagonalizável.
	2. Forme a matriz P = $[p_1~~~ p_2 ~~~· · ·~~~ p_n ]$ que tem os vetores de S como vetores coluna.
	3. A matriz $P^{-1}AP$ será diagonal com os autovalores $\lambda_1 ,\lambda_2 , . . . , \lambda_n$ n correspondentes aos autovetores $p_1 , p_2 , . . . , p_n$ como entradas diagonais sucessivas.

	Octave:  encontrar a diagonal da matriz A
	```octave
	A = [2,-1,-1
		-1,2,-1      # Matrix que queremos diagonalizar
		-1,-1,2]      

	[V, D] = eig(A) # Encontra a diagonal (D) e a matrix P(V)
	V*D*inv(V)
	```
	
	- Exemplo
		Encontre uma matriz P que diagonalize A
			$A = \begin{bmatrix} 0 & 0 & -2\\ 1 & 2 & 1\\ 1 & 0 & 3\end{bmatrix}$; Os auto valores são $A-\lambda$ = $A = \begin{vmatrix} \lambda -0 & 0 & -2\\ 1 & \lambda -2 & 1\\ 1 & 0 & \lambda -3 \end{vmatrix} =0 =\lambda^3 -5\lambda^2+8\lambda-4 = (\lambda-1)(\lambda-2)^2$
			
		Podemos encontrar as bases caso $\lambda=1 ~ou~ 2$
		$\lambda =1$ ->$$\begin{bmatrix} -2\\ 1\\ 1 \end{bmatrix}$$
		$\lambda =2$ --> $\begin{bmatrix}-1\\0\\1 \end{bmatrix}$ e $\begin{bmatrix} 0\\ 1\\ 0\end{bmatrix}$
		Então a matriz P é $P = \begin{bmatrix} -1 & 0 & -2\\ 0& 1& 1\\ 1 & 0 &1\end{bmatrix}$ ; para diagonalizar fazemos $P^{-1}AP$

| Propriedade              | Descrição                                               |
| ------------------------ | ------------------------------------------------------ |
| Determinante             | A e $P^{-1}AP$ têm o mesmo determinante                |
| Invertibilidade          | A é invertível se e somente se,$P^{-1}AP$ é invertível |
| Posto                    | A e $P^{-1}AP$ têm o mesmo posto                       |
| Nulidade                 | A e $P^{-1}AP$ têm a mesma nulidade                    |
| Traço                    | A e $P^{-1}AP$ têm o mesmo traço                       |
| Polinômio característico | A e $P^{-1}AP$ têm o mesmo polinômio caracteristico    |
| Autovalores              | A e $P^{-1}AP$ têm os mesmos autovalores               |
| Dimensão do autoespaço   | Se $\lambda$ for um autovalor de A e,portanto, de $P^{-1}AP$, então o autoespaço de A associado a $\lambda$ e ao autoespaço de $P^{-1}AP$ tem a mesma dimensão                                                       |
### Teorema
-> Se uma matriz A de tamanho $n \times n$ tem $n$ autovalores distintos, então A é diagonalizável 
**Se for uma matriz simétrica**

Algoritmo:
	==1== . Encontre as bases associadas a cada autovalor
	==2== . Aplique o [[Processo de Gram-Schmidt]] para encontrar a base ortonormal  de cada espaço
	==3== . Forma a matriz p com as bases encontradas no passo 2 da forma $P^tAP=D$ e encontre a diagonal
 - ## [[Matriz ortogonal]]

Uma matriz ortogonal é dita ortogonal se sua inversa coincide com sua transposta
$$Se~~Q^{-1}=Q^t ~\Rightarrow ~\text{Q é ortogonal}$$

$Q= [\vec u_1 , \vec u_2 ... ,\vec u_n]$ uma matriz ortogonal de ordem NxN. Então para quaisquer vetores $\vec v$ e $\vec  w$ em $R^n$ temos:

| Propriedade conservada                          | descrição                                |
| ----------------------------------------------- | ---------------------------------------- |
| $Q \vec v \cdot Q \vec w = \vec v \cdot \vec w$ | O produto euclidiano é conservado(Norma) |
|$\|(Q \vec v)\|  =  \|(\vec v)\|$                   |            Conserva a norma                             |
|                      freferg                           |               o ângulo entre $Q \vec v$ e  $Q \vec w$ é igual ao ângulo entre $\vec v$ e $\vec w$                          |


