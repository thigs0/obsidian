**Podemos entender por variável aleatória como um característico numérico do resultado de um experimento.**

_Exemplo_:
	1. $\large \epsilon$ lançar uma moeda n vezes 
		$\large \Omega= \{\omega_1, \omega_2, \omega_3,...\omega_n\}: \omega_i=C ~ou~\bar C$ 
		$X(\omega)$ = Número de caras em $\omega$ ou $\begin{cases} i,w_i=C ~|~ i=1,2,3,...n\end{cases}$
	2. $\large \epsilon$ Escolher um ponto ao acaso no intervalo [0,1].
		$\Omega = [0,1]$ 
		$X(\omega) = w^2$
	3. $\epsilon$ Selecionar um aluno ao acaso de ME210
		$\Omega= \{\text{Alunos de ME210}\}$
		$X(\omega) =$ altura do aluno

- ***Definição** [[Variável Aleatória]]
	Uma variável aleatória (V.A) X em um espaço de probabilidade espaço amostral, [[Sigma-álgebra]] e a probabilidade ($\Omega , \mathscr{A}, P$) é uma [[Funções]] real definida em $\Omega$, 
	$$\begin{matrix} X:\Omega \rightarrow \Re \\\omega \rightarrow X(\omega)\end{matrix}$$
	Tal que $\large \{ \omega \in \Omega : X(\omega) \leq r\} \in \mathscr{A},~ \forall r \in \Re$
	_**Exemplos**_:
		1. $\large \epsilon$: lançamento de uma moeda honesta três vezes
			$\Omega=\{(\omega_1, \omega_2\omega_3) : \omega_i= C~ou~\bar C\}$
			$X:$ Numero de caras
			$\mathscr{X}$= {0,1,2,3}: conjunto de valores possíveis de X
			P($\mathscr{X}=0$) = P({$\bar C, \bar C, \bar C$}) = $\displaystyle \frac{1}{8}$  
			P($\mathscr{X}=1$) = P({$(C, \bar C, \bar C), (\bar C, C \bar C),(\bar C , \bar C ,C)$}) = $\displaystyle \frac{3}{8}$
			P($\mathscr{X}=2$) = $\displaystyle \frac{3}{8}$
			P($\mathscr{X}=3$) = $\displaystyle \frac{1}{8}$

| x   | P($\mathscr{X}=x$) |
| --- | ------------------ |
| 0   | 1/8                |
| 1   | 3/8                |
| 2   | 3/8                |
| 3   | 1/8                |
|     |                    |
		2. 3 Bolas retiradas sem reposição de uma urna com 20 bolas numeradas de 1 a 20
		 X: O maior número selecionado
		 P($\mathscr{X}=10$) = $\displaystyle \frac{\begin{pmatrix}1 \\1\end{pmatrix}\cdot \begin{pmatrix}9 \\2\end{pmatrix}}{\begin{pmatrix}20 \\3\end{pmatrix}} = \frac{36}{1140}$
		De forma geral
		$\displaystyle P(\mathscr{X}=i)= \frac{\begin{pmatrix}1 \\ 1\end{pmatrix}\cdot \begin{pmatrix}i-1 \\2\end{pmatrix}}{\begin{pmatrix}20 \\3\end{pmatrix}},~i=3,...,20$

[[Variáveis aleatórias discretas]]
	Uma V.A $\large \mathscr{X}$ é discreta se assume valores em um conjunto finito ou enumerável.
	$\displaystyle \large X :\Omega \rightarrow \mathscr{X} =\{x_1,x_2,x_3,...,x_n\}$
	_Exemplos:_
	1. Contagens
		$\mathscr{X}$ = Nº de partículas emitidas por uma fonte radioativa, $\mathscr{X} = \mathscr{N}$
	2. 
	   $\begin{cases}1, \text{ Se sair C}\\ 0, \text{Se sair C'} \end{cases}$
	   $\Omega = \{C , C'\} \rightarrow \mathscr{X}=\{0,1\}$
[[Função de probabilidade]]
	Para uma V.A discreta $\mathscr{X}$, a função de probabilidade $f_p$ de $\mathscr{X}$, denota por p(x), é dada por:$$p(x)= P(\mathscr{X}=x),~~x \in \mathscr{X}$$
	_Exemplos:_
		1. No exemplo do lançamento de uma moeda 3 vezes. 
		 p(x) = P$(\mathscr{X}=x)= \begin{cases}1/8, \text{Se x=0,3}\\ 3/8 ,~\text{Se x=1,2}\\ 0 , \text{caso contrário(C.C)}\end{cases}$
	
$\textbf{Definição}$: [[Função de distribuição acumulada]]:
	A função de distribuição acumulada (fda) de uma V.A $\mathscr{X}$ é dada por $$F(x) = P(\mathscr{X}\leq x);~~~x \in \Re$$
**Definição**: Valor esperado ou [[Esperança]]
	$\displaystyle \large E(x) = x_1p(x_1) + x_2p(x_2)+x_3p(x_3)+...+x_np(x_n) = \sum_{i=1}^n x_ip(x_i)$ 
| Propriedade                       | Nº  |
| --------------------------------- | --- |
| $E(k)=k; ~~k \in \mathbb{R}$      | (1) |
| $E(Kx) =KE(x), ~~k\in \mathbb{R}$ | (2) |
| $E(X\pm Y) = E(X) \pm E(Y)$       | (3) |

**Definição**: [[Variância]]
	$Var(x) = E[(x-\mu)^2]$; $\mu$ é a média
	**Proposição**: A Var(x) = $E(x^2)-E^2(x)$ -> A variância é o valor esperado de x ao quadrado menos o valor esperado ao quadrado de x
	*Dem* (Caso discreto)-> 
	$\displaystyle var(x)= E[(x-\mu)^2] \xRightarrow {g(x)= (x-\mu)^2} \sum_x (x-\mu)^2p(x)= \sum_x (x^2-2\mu x + \mu^2)p(x)= \sum_x x^2p(x) -2\mu \sum_x  x p(x) +\mu ^2 \sum_x  p(x)$
	-> $E(x^2) - 2\mu \mu + \mu^2 1 \Rightarrow E(x^2)- 2 \mu^2+ \mu^2 = E(x^2)-\mu^2 = E(x^2)-E^2(x)$
	*Exemplo*:
	$\Large \epsilon$: lançamento de um dado honesto
	X: Número de faces
	.
	E(x) = $\displaystyle \sum_x xp(x)= 1.\frac{1}{6}+ 2.\frac{1}{6} + 3\frac{1}{6}+ 4\frac{1}{6} +5 \frac{1}{6} +6\frac{1}{6} =\frac{7}{2}$ 
	E(x²) = $\sum_x x^2p(x) = 1^2.\frac{1}{6} + 2^2. \frac{1}{6} +3^2.\frac{1}{6}+4^2.\frac{1}{6}+5^2\frac{1}{6}+6^2.\frac{1}{6} = \frac{91}{6}$
	Var(x) = $\displaystyle E(x^2)-E^2(x) = \frac{91}{6}-\left( \frac{7}{2}\right)^2 = \frac{35}{12}$
	**Proposição**: $Var(ax+b) = a^2. var(x), a,b \in \Re$ 
	*Dem*: $E(ax+b) = aE(x)+b = a \mu +b$
	-
	$\large var(ax+b) \xRightarrow {\text{pela definição}} E[(ax+b- a \mu -b)^2]=E[(a^2.(x-\mu)^2)]= a^2 E((x-\mu)^2) = a^2 var(x)$
	*Exemplos*:
	(1) no exemplo anterior
	Var(2x+5) = 2²Var(x) = $\displaystyle 4\frac{35}{12}= \frac{35}{3}$ 
	(2) F = $\displaystyle \frac{9C}{5}+32$
	Var(F) = var($\frac{9c}{5}+32$) = (9/5)² var(c) = $\displaystyle \frac{81}{25}var(C)$
(1) $Var(x) \geq 0$ 
(2) A unidade de medida da variância é o quadrado da unidade da variável aleatória
(3) O [[Desvio padrão]] de x é dado por  $SD(x) = \sqrt{Var(x)}$ 
(4) Para [[Distribuição de Bernoulli]]$\displaystyle \large \sum_x xp(x) = 0(1-p) +1p \Rightarrow E(x)=p$
	E($x^2$) = $\displaystyle \sum_x x^2p(x) = 0^2(1-p) +1^2.p = p$
	Var(x) = $E(x^2)-E(x^~2) = p-(p^2)= p(1-p)$
		











	