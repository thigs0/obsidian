**Definição**: Norma de um vetor em $\mathscr{R}^n$ é uma função ||.|| : $\mathscr{R}$ -> $\mathscr{R}$ que satisfaz as seguintes propriedades
	1. $||x|| \geq 0, ~ \forall x \in \Re^n$ e $||x||=0$ se e somente se $x=0$
	2. $||\alpha x|| = |\alpha| |x|, ~ \forall x \in \Re^n$ e V$\alpha \in \Re$ 
	3. $||x+y|| \leq ||x||+||y||$, $\forall x,y ~ \in ~\Re^n$ ([[Desigualdade triangular]])

**Exemplo**:
	A norma Euclidiana (ou norma 2)
	$\displaystyle ||x||_2 = \left( \sum_{i=1}^n|x_i|^2\right)^{1/2}$ com $x=(x_1,...,x_n)^T \in \Re^n$
	Os índices 1 e 2, são diretos. O 3 necessita da [[Desigualdade de Cauchy-Schwarz]]

#### Teorema:
	$\large \forall n,y \in \mathbb{R}^n,~ ||x+y||_2 \leq ||x||_2 +||y||_2$
		Dem: Validamos para o quadrado de ambos os lados
		$<x+y,x+y> \leq (\sqrt{<x,x>} + \sqrt{<y,y>})^2 ~= ~ <x,x> + 2\sqrt{<x,x><y,y>} + <y,y>$
		Como <x,x> e <y,y> são maiores ou iguais à 0, o aldo esquerdo é menor ou igual ao lado direito
**Definição**;
	A distância entre dois vetores x e y é dada por:
	$$||x-y||_2 = \sqrt{\sum_{i=1}^n\left(x_i-y_i\right)^2}$$
	Exemplos de P-Norma:
		1. $||x||_1 = \sum_{i=1}^n |x_i|$ -> Norma 1
		2. $||x||_\infty = max |x_i|$ -> Norma infinita
		3. $||x||_p = \left(\sum_{i=1}^n |x_i|^p\right) ^{1/p}$


Sejam A,B $\in \mathbb{R}^{m,n}$ e $\alpha \in \mathbb{R}$
	- [[Matriz Transposta]]:
		$A^T=C$=> $C_{ij}=a_{ji}, ~\forall i,j$
	- Adição de matrizes
	- Multiplicação por escalar
	- Multiplicação de matriz
		$A \in \mathbb{R}^{m,r}$ e $B \in \mathbb{R}^{r,m}$
		C = AB => $\displaystyle c_{ij} = \sum_{k=1}^{r} a_{ik}. b{kj}$
	- [[Matriz inversa]]
		$C= A^{-1}$
		Se m=n, então CA = AC= I
	- [[Produto interno]]
		$x,y \in \mathbb{R}^n$
		$x^Ty = C$ => $\displaystyle \sum_{i=1}^n x_iy_i = c$

**Definição**:
	A norma de uma matriz é uma função $||.|| \mathbb{R}^{n_xn}$ -> $\mathbb{R}$ que satisfaz as seguintes propriedades
	Para todo $A,B \in \mathbb{R}^{n_n}$ e $\alpha \in \mathbb{R}$
	1. $||A|| > 0$, se $A \neq 0$ e $||A|| =0$ se e somente se $A=0$
	2. $||\alpha A|| = ||\alpha||.||A||$
	3. $||A+B|| \leq ||A||+||B||$
	4. $||AB|| \leq ||A||.||B||$ (Consistência)
	**Exemplos**
	a) $\displaystyle ||A||_F = \left(\sum_{j=1}^n \sum_{i=1}^n |a_{ij}|^2\right)^{1/2}$ [[Norma de Frobenius]]
	b) [[Norma induzida]] - Dada a função norma de vetor $||.||_v$, a norma de [[Matriz]] induzida por $||.||_v$ é definido por$$\displaystyle ||A|| = max_{X \neq 0} \frac{||AX||_v}{||X||_v}$$
**Teorema**
	$||AX|| \leq ||A||.||X||$
	*Dem*: Para o vetor nulo temos a igualdade 0=0
		 Caso contrário, $\displaystyle \frac{||AX||}{||X||} \leq ||A||$ usando a norma induzida $\displaystyle \frac{||AX||}{||X||} \leq max_{X \neq 0} \frac{||AX||_v}{||X||_v}= ||A||$  

**Exemplo**:
	a) $\displaystyle ||A||_1 = max_{1 \leq j \leq n} \sum_{i=1}^n |a_{ij}|$ -> Norma 1 ou Norma coluna (Percorre a coluna somando os módulos e no final pega o máximo)
	b) $\displaystyle ||A_\infty|| = max_{1 \leq i \leq n}\sum_{j=1}^n |a_{ij}|$ -> Norma infinita ou norma linha

```julia
function NormaColuna(A)
	#Matriz A quadrada
	a,b = size(A);
	#tratamento de erros
	if a != b
		return -1;
	end
	
	maior = 0;
	for i in 1:a
		coluna =0
		for j in 1:a
			coluna += abs(A[i, j])
		end;
		if (coluna > maior)
			maior = coluna;
		end
	end
	return maior;
end


function NormaLinha(A)
	# Matriz A quadrada
	a,b = size(A);
	#tratamento de erros
	if a != b
		return -1;
	end
	
	maior = 0;
	for i in 1:a
		linha =0;
		for j in 1:a
			linha += abs(A[j, i]);
		end
		if (linha > maior)
			maior = linha;
		end
	end
	return maior;
end

function NormaFrobenius(A)
	# Matriz A quadrada de floats
	a,b = size(A);
	#tratamento de erros
	if a != b
		return -1;
	end

	maior=0;
	for i in 1:a
		for j in 1:a
			maior += abs(A[i, j])^2;
		end
	end
	return sqrt(maior);
end
```


