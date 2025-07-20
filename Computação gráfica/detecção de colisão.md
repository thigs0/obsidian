### Árvore AABB
- usamos o conceito de [[Árvore binária]] para buscar colisões
- Uma ávore AABB é uma estrutura espacial construída de forma [[Recursiva]] sobre um objeto (malha)
```cpp
struct AABBnode{
	AABBleft* left;
	AABBright* right;
	AABBtype AABB
}

struct AABBtree{
	AABBnode * root;
	build(root)// recursive method to construct the tree
}
```
- usando a àrvore, dividimos o espaço de maneira recursiva com um critério de parada podendo ser o tamanho que gere um pixel.
- Encontramos a intersecção entre as folhas e então analisaremos a intersecção entre triângulos

**Ideia de algoritmo para criar a estrutura**
***Construção da AABB tree***
-> Segue a abordagem top-down com divisão recursiva dos AABBs
***Caso Base***
-> Se o conjunto de triângulos possui apenas triângulos. Então cria-se um nó desse triângulo e retornamos
***Caso recursivo***
- Calcula-se a AABB para todos os triângulos de entrada
- Escolher o eixo de divisão (o mais largo)
- Ordenamos os triângulos pelo centroide do eixo de divisão
- Divide-se o conjunto de triângulos em dois subconjuntos **left** e **right** 

**Detecção de colisão entre duas AABB**
1) Comece comprovando os nós raiz de ambas as árvores
2) Se as AABBs não se interseptão descarte as sub-árvores
3) Se existe intersecção:
	1) Se ambos são folhas: Encontre a colisão entre triângulos
	2) Caso contrário, avance recursivamente para cada filho

### Algoritmo Moller-Trumbore intersecção de raio-triângulo
- Dado um raio ([[Vetor]]) $R=0+td$
onde                 $\begin{align} o:\text{origem do raio (ponto inicial)} \\ d:\text{vetor direção}\\ t:\text{Escalar}, t\in[0,\infty]\end{align}$
- Um triângulo definido pelos vértices $v_0,v_1,v_2$
Queremos determinar se o raio fura o triângulo e calcular o ponto de furo.

##### Algoritmo
1) Determine duas arestas do triângulo 
	- $e_1=V_1-v_0$
	- $e_2=V_2-V_0$
2) Ponto de interseção
	- $P=V_0-ue_1+Ve_2,~~u\geq 0, V\geq 0, u+V \leq 1$
3) Equação do raio e ponto-triângulo
	- $o+td=V_0+ue_1+Ve_2$
	- $\begin{bmatrix}...  & ... & ...\\ e_1 & e_2 & t\\... & ... & ...\end{bmatrix}\begin{bmatrix}u\\ v\\ t\end{bmatrix}=o-V_0$
	1) Para resolver, primeiro calculamos o [[Produto vetorial]] $\rho=d\times e_2$
	2) Calcular o determinante $det =e_1\cdot \rho$ 
	- Se $\|det\|\leq \epsilon$ o raio é paralelo ao triângulo
	- Calcular o vetor $t=o-V_0$
	- Calcular u $\displaystyle u=\frac{T\cdot \rho}{det}$
	- Se $u<0$ ou $u>1$, não há intersecção
	- Calcule o vetor  $q=t\times e_1$
	- Calcular $v=\displaystyle \frac{d\cdot q}{det}$
	- Se $v\notin [0,1]$ o ponto está para fora do triângulo
	- Calcule $t=\frac{e_2\cdot q}{det}$
	- Se t<0 a intersecção está atrás da origem do raio
**Exemplo**
$\begin{align} o=\begin{bmatrix} 0.25 & 0.25 & 1\end{bmatrix}\\ d=\begin{bmatrix} 0 & 0 & -1\end{bmatrix}\\ V_0=\begin{bmatrix} 0 & 0 & 0 \end{bmatrix}\\ V_1=\begin{bmatrix} 1 & 0 & 0\end{bmatrix}\\ V_3=\begin{bmatrix} 0 & 1 & 0\end{bmatrix}\end{align}$
- **Calcular as arestas**
$e_1=V_1-V_0=\begin{bmatrix} 1 & 0 & 0\end{bmatrix}$
$e_2=V_2-V_0=\begin{bmatrix} 0 & 1 & 0\end{bmatrix}$
- **Calcular $\rho =d\times e_2$**
$\rho =\begin{bmatrix} 0,0,-1\end{bmatrix}\times \begin{bmatrix} 0 & 1 & 0\end{bmatrix}=\begin{bmatrix} 1 & 0 & 0\end{bmatrix}$
- **calcular a determinante** $det=e_1\cdot \rho$
$det=\begin{bmatrix} 1 & 0 & 0\end{bmatrix}\cdot \begin{bmatrix} 1 & 0 & 0\end{bmatrix}=1$ 
- **Calcular o vetor** $t=o-V_0$
$T=\begin{bmatrix} 0.25 & 0.25 & 1\end{bmatrix}-\begin{bmatrix} 0 & 0 & 0\end{bmatrix}=\begin{bmatrix} 0.25 & 0.25 & 1\end{bmatrix}$
- **calcular** $u=\frac{T\cdot P}{det}$
$u=\frac{\begin{bmatrix} 0.25 & 0.25 & 1\end{bmatrix}\cdot \begin{bmatrix} 1 & 0 & 0\end{bmatrix}}{1}=0.25$
- **calculamos** $q=T\times e_1$
$q=\begin{bmatrix} 0.25 & 0.25 & 1\end{bmatrix}\times \begin{bmatrix}1 & 0 & 0 \end{bmatrix}=\begin{bmatrix} 0 & 1 & -0.25\end{bmatrix}$
- **Calcule** $V=\frac{d\cdot q}{det}$
$v=\begin{bmatrix} 0 & 0 & -1\end{bmatrix}\cdot \begin{bmatrix} 0 & 1 & -0.25\end{bmatrix}=0.25$ 
- **Se está dentro do triângulo**
Todos são válidos

- **calcular** 
- $t=\frac{e_u\cdot q}{det}=\frac{\begin{bmatrix} 0 & 1 & 0\end{bmatrix}\cdot \begin{bmatrix} 0 & 1 & -0.25\end{bmatrix}}{1}=1$
- Ponto de interseção

### [[Teorema do eixo-separador]]
- Verificar interseção entre triângulos
- Dois triângulos não se tocam se e somente se existe um eixo ao longo do qual a projeção não se sobrepoem
Para triângulos podemos reduzir a poucos considições
1) normais dos triângulos
2) vetores cruzados entre arestas de A e B

Dados dois triângulos A e B com vértices $A_i$ e $B_i$ ; $i\in [ 0,1,2 ]$
e [[vetores]] normais $N_A$ e $N_B$

1) Calcular os eixos candidatos:
	1) Normais dos triângulos (2 eixos possíveis)
	2) Produtos vetoriais das arestas (9 arestas)
	3) Para cada aresta $e_A$ e $e_B$ Calculamos
	$$d=e_A\times e_b$$
	- Se $d=0$, as arestas são paralelas, ignoramos outros d
2) Projetar os triângulos em cada eixo para cada eixo $d$. Calcular o intervalo de projeção
	$$Proj_d(A)=[ \min A^td, \max A^td ]$$
	$$Proj_d(B)=[ \min B^td, \max B^td ]$$
3) Verificar sobreposição
Se $\max A<\min B \~~\land \max B<\min A$ então os triângulos não se interseptão


**Exemplo 3D**
$A_1=\begin{bmatrix} 0 & 0 & 0 \end{bmatrix}$
$A_2=\begin{bmatrix}1 & 0 & 0\end{bmatrix}$
$A_3=\begin{bmatrix}0 & 1 & 0\end{bmatrix}$

$B_1=\begin{bmatrix}0.5 & 0.5 & 1\end{bmatrix}$
$B_2=\begin{bmatrix}0.5 & 0.5 & -1\end{bmatrix}$
$B_3=\begin{bmatrix}1 & 1 & 0\end{bmatrix}$

1) **Encontramos as normais**
$N_A=\begin{bmatrix}0 & 0 & 1\end{bmatrix}$
$N_B=\begin{bmatrix}2 & -2 & 0\end{bmatrix}$

2) **produto vetorial para todas arestas**
$e_{A_1}=A_2-A_1=\begin{bmatrix}1 & 0 & 0\end{bmatrix}$
$e_{A_2}=A_3-A_2=\begin{bmatrix}-1 & 0 & 0\end{bmatrix}$
$e_{A_3}=\begin{bmatrix}0 & -1 & 0\end{bmatrix}$
$e_{B_1}=\begin{bmatrix} 0 & 0 & -2 \end{bmatrix}$
$e_{B_2}=\begin{bmatrix}0.5 & 0.5 & 2\end{bmatrix}$
$e_{B_3}=\begin{bmatrix}-0.5 & -0.5 & 1\end{bmatrix}$

 