	- Generalização de Bernouli

Considere uma sequência de n [[Variável Aleatória]]s com [[Distribuição de Bernoulli]] com parâmetros p independentes.
	$X_1, X_2, X_3,...X_n$, -> $X_i$~$Ber(p)$ 
Definimos a variável aleatória como:
	X = $X_1+X_2+X_3+...+X_n$ -> Contagem do número de sucessos que retiramos em n tentativas
	$p(x) = P(X=x)$, n=5 e P(X=3 caras) P(X=3) = $\displaystyle \begin{pmatrix}  5\\ 3\end{pmatrix}\left ( \frac{1}{2}\right)^3 \left( 1 - \frac{1}{2}\right)^2$ 
	$\displaystyle \large p(x) = P(X=x) =\begin{pmatrix}  n\\ x\end{pmatrix} p^x(1-p)^{n-x} \mathbb{I}_{\{0,1,2....,n\}}^{(x)}$ e dizemos que X ~ Bin(n,p)


 **Obs 1**:  $Bin(1,p) = Ber(p)$
 **Obs 2**: $\displaystyle \sum_{x=0}^n p(x) = \sum{x=0}^n \begin{pmatrix} n \\x\end{pmatrix} p^x (1-p)^{n-x}$ 
 **Obs 3**: Sabemos que $x \begin{pmatrix} n \\ x\end{pmatrix} = n\begin{pmatrix} n-1 \\ x-1\end{pmatrix}$
	 $\displaystyle E(x^k) = \sum_{x} x^k \cdot p(x)= \sum_x x^k \begin{pmatrix} n \\ x\end{pmatrix} p^x (1-p)^{n-x} = \sum_{x=1}^n x^{k-1}x \begin{pmatrix} n \\ x\end{pmatrix} p^x (1-p)^{n-x}$ ,x=0 ->0
	 $\displaystyle \sum_{x=1}^n x^{k-1}\cdot n\begin{pmatrix} n-1 \\ x-1\end{pmatrix} . p p^{x-1}(1-p)^{n-x}$ 
	 $\displaystyle n.p \sum_{x=1}^n x^{k-1}\begin{pmatrix} n-1 \\ x-1\end{pmatrix}p^{x-1}(1-p)^{n-x} \xRightarrow {y=x-1} np \sum_{y=0}^{n-1} (y+1)^{k-1} \begin{pmatrix} n-1 \\ y\end{pmatrix} p^y(1-p)^{(n-1)-y}$ 
	 -> Os 3 últimos parâmetros formam um Bin(n-1,p) 
	 = $\displaystyle \large np. E[(y+1)^{k-1}]$ 
	 Logo: $\large E(x^k) = np. E[(y+1)^{k-1}]$ para $k \in \mathbb{N}$
	*Exemplo*:
	$E(X^1) = E(x) = npE((Y+1)^{1-1}) = np$ 
	$E(X^2) = npE[(Y+1)^{2-1}] = np E[Y+1] = np[E(Y)+1] = np[(n-1)p+1] = (np)^2 -np^2 +np$ 
	Var(x) = $E(x^2) - E^2(x) = (np)^2 -np^2 +np -(np)^2 = np -np^2 = np(1-p)$ 
**Obs 4:**
	X~ Bin(n,p) e Y ~ Bin(n, p) são independentes <=> X+Y ~ Bin(n+m, p)



*Exemplos*
(1) $\epsilon$: Lançar uma moeda honesta 5 vezes
	X: # caras
	X~Bin(5, 1/2) ; n-> 5, 1/2 -> p
	P(x) = $\displaystyle \large \begin{pmatrix}  5\\ x\end{pmatrix} (1/2)^x(1-1/2)^{5-x} \mathbb{I}_{\{0,1,2....,5\}}^{(x)}$
(2) Pacote com 10 parafusos. O pacote será trocado se possuir mais do que 1 parafuso defeituoso.
	A probabilidade do parafuso ser defeituoso é p=0.01
	n<- 10, p <- 0.01
	p(x) =$\displaystyle \large \begin{pmatrix}  10\\ x\end{pmatrix} 0.01^x(1-0.01)^{10-x} \mathbb{I}_{\{0,1,2....,10\}}^{(x)}$
	A probabilidade de ser trocado
	P(X>1) = 1- P(X=1) - P(X=0) = 0,004 