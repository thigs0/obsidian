
Probabilidade de um evento, sabendo que já ocorreu um evento que afeta ele

$\large \textbf{Definição}$ **(Probabildiade condicional)**
	Seja ($\Omega$, $\mathscr{A}$=[[Sigma-álgebra]], P) um espaço de probabilidade. Se $B \in A \in P(B) >0$ Então, a probabilidade condicional de $\alpha$ dado  a ocorrencia de B é definida por: $$P(A|B) = \frac{P(A\cap B)}{P(B)}, ~~\forall \alpha \in A$$
	_OBS_:
		Verifica-se que $P(\cdot |B)$ é uma probabilidade em [[Sigma-álgebra]], isto é, esta função satisfaz os [[Axiomas de Kolmogorov]]
		  Para o primeiro axioma
			$\displaystyle 0 \leq \frac{P(º \cap B)}{P(B)} \leq 1 \Rightarrow 0 \leq P(º \cap B) \leq P(B)$ 
			$º \cap B$ é no mínimo é vazio, e, $P(\emptyset) =0$ 
		Para o segundo axioma
			$\displaystyle P(\Omega|B) = \frac{P(\Omega \cap B)}{P(B)} = \frac{P(B)}{P(B)} =1$
		Para o terceiro axioma
			$\displaystyle P(U_{i=1}^\infty|B) = \frac{P(U_{i=1}^\infty)\cap B}{P(B)} = \frac{U_{i=1}^\infty (A_i \cap B)}{P(B)}$ como os Ais são disjuntos
			$\displaystyle \frac{P(A_1 \cap B)}{P(B)} + \frac{P(A_2 \cap B)}{P(B)} + ... = \sum_{i=1}^\infty P(A_i |B)$ 
		
_Exemplo_:
	A população de um país consiste em 3 grupos étnicos. Além dsso, cada indivídup pertence a um de 4 grupos sanguineos. A tabela apresenta as probabilidades conjuntas das combinações dos grupos.
	| Grupo étnico \ Grupo Sanguineo | O     | A     | B     | AB    |
	| ------------------------------ | ----- | ----- | ----- | ----- |
	| 1                              | 0,082 | 0,106 | 0,008 | 0,004 |
	| 2                              | 0,135 | 0,141 | 0,018 | 0,006 |
	| 3                              | 0,215 | 0,200 | 0,065 | 0,020 |
	Se um indivídeo é selecionado aleatóriamente, qual a probabilidade de pertencer ao grupo sanguineo A dado que pertence ao grupo étnico 3?
	A: grupo sanguineo A
	B: Grupo étnico 3
	$\displaystyle P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{0,2}{0,5}= 0,4$

**[[Teorema da multiplicação]]**
	(i)   $\large P(A \cap B) = P(B) . P(A|B) = P(A). P(B|A)$
	(ii)  $P(A_1 \cap A_2 \cap ... \cap A_n) = P(A_1)P(A_2 | A_1)P(A_3|A_1\cap A_2)....P(A_n|A_1 \cap A_2 \cap ... \cap A_{n-1}),$
		$\forall A_1,A_2,...A_n \in Sigma-Algebra, \forall n \geq 2$
**[[Teorema da probabilidade total]]**
	Se $A_1, A_2,...$ formam uma partição de $\Omega$, Então:
	A probabilidade de ocorrer um evento B $\large \displaystyle P(B)= \sum_{i=1}^{\infty} P(A_i)P(B|A_i)$
	Demonstração: 
		B = $(B \cap A_1) \cup (B \cap A_2) \cup ... (B \cap A_n) \Rightarrow U_{i=1}^{\infty} (B \cap A_i)$ 
		Assim, $\large \displaystyle  P(B) =P(U_{i=1}^{\infty} (B \cap A_i)) \xRightarrow[Axioma~3] ~\sum_{i=1}^{\infty} P(B\cap A_i) \xRightarrow[Teorema~da~multiplicacao]~ \sum_{i=1}^{\infty} P(A_1)P(B|A_i)$
		.
	Definição de uma partição:  $A_1, a_2, A_3...$ é partição de $\Omega$ se $\displaystyle \large A_1 \cap A_j = \emptyset ~~~ \forall i \neq j \in U_{i=1}^{\infty}A_i = \Omega$
	.
	_Exemplo_
		Considere um lote com 20 peças defeituosas e 80 não defeituosas. Extraímos duas peças sem reposição.
		1. Qual a probabilidade de que ambas sejam defeituosas? 
			A: 1ª peça  defeituosa
			B: 2ª peça defeituosa 
			P($A \cap B$) = $\displaystyle P(A). P(B|A)= \frac{20}{100} \frac{19}{99} = \frac{19}{495}$
		2. Qual a probabilidade de que a 2ª peça seja defeituosa?
			A: primeira peça é defeituosa
			B: 2ª segunda defeituosa
			$\displaystyle P(B) = P(A).P(B|A) + P(A^c) P(B|A^c) = \frac{20}{100}\frac{19}{99} + \frac{80}{100}\frac{20}{99} = \frac{1}{5}$
			
			
**[[Teorema de Bayes]]**
	Se $A_1, A_2,...$ formam uma partição de $\Omega$, então$$\displaystyle \large P(A_i|B) = \frac{P(A_i)P(B|A_i)}{\sum_{j=1}^{\infty}P(A_j)P(B|A_j)};~~~ \forall B \in sigma-algebra$$
	Dem:
		$\large \displaystyle P(A_i|B) = \frac{P(A_i \cap B)}{P(B)} \xRightarrow[\text{Teorema da probabilidade Total}] {teorema~da~multiplicação} \frac{P(A_i).P(B|A_i)}{\sum_{j=1}^{\infty} P(A_j)P(B|A_j)}$
	_Exemplo_
		Apenas 1 em 1000 adultos é acometido por uma doença, a qual foi desenvolvido um teste diagnóstico. Neste teste, se o indivíduo tiver a doença, o teste será positivo em 99% das vezes e, se não tiver, será positivo em 2% das vezes. Se um indivíduo selecionado testou positivo, qual a probabilidade de ter a doença?
		A: tem a doença
		B: testar
		P(A) = 0,001
		P(B|A) = 0,99
		P(B|$A^c$) = 0,02
		P(A|B) = $\displaystyle \frac{P(A)P(B|A)}{P(A)P(B|A)+P(A^c)P(B|A^c)} = \frac{0,001.0,99}{0,001.0,99+0,999.0,02}= 0,047$
		

## [[Independência]]
Dois eventos podem ser definidos dependentes se a ocorencia de um evento A influencia em alguma instância o evento B
```graph
Evento A -> Evento B
```
**Definição**
	Seja $(\Omega, A, P)$ um espaço de probabilidade. Os eventos aleatórios A e B são independentes se, se somente se, a probabilidade $P(A \cap B) = P(A).P(B)$
	.
	_exemplo_:
		1. $\epsilon$: lançamentos de 2 moedas honestas
			A: Face cara na 1º moeda
			B: Face cara na 2º moeda
			
			$\large \Omega = {(c, \bar c), (\bar c, c), (c,c), (\bar c , \bar c)}$
			$\displaystyle P(A \cap B) = \frac{\# A \cap B}{\# \Omega}= \frac{1}{4}$
			$\displaystyle P(A)= \frac{\# A}{\# \Omega}= \frac{2}{4}= \frac{1}{2}$
			$\displaystyle P(B) = \frac{\# B}{\# \Omega}= \frac{2}{4} =\frac{1}{2}$
		2. $\epsilon$: Lançamento de 2 dados honestos
			A: O 1º dado é par
			B: O 2º dado é 5 ou 6
			
			$\Omega = {(i,j); i,j=1,...,6}$
			$\displaystyle P(A \cap B) = \frac{6}{36}$
			$\displaystyle P(A) = \frac{18}{36} = \frac{1}{2}$
			P(B) = $\displaystyle \frac{12}{36} = \frac{1}{3}$
	**Definição** ([[Eventos coletivamente independentes]])
		Os eventos $A_1,A_2,A_3,...A_n$ são coletivamente independentes se $P(A_{i_1} \cap A_{i_2} \cap ... \cap A_{i_m}) = P(A_{i_1}).P(A_{i_2})...P(A_{i_n});~~ \forall 1 \leq i_1 < i_2<i_3<...<i_m \leq i_n;~~~\forall m= 2,3,...n$
		_Exemplo_:
			A,B e C são coletivamente independentes se $$\begin{cases}P(A \cap B)= P(A).P(B \\ P(A \cap C) =P(A).P(C) \\ P(B \cap C) = P(B).P(C) \\ P(A \cap B \cap C) = P(A).P(B).P(C)\end{cases}$$
		
| Nº  | propriedades                                                                    | descrição                                                                                    |
| --- | ------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| 1   | A e B disjuntos ($A \cap B= \emptyset$ \~$\leftrightarrow$ A e B independentes) | Se dois eventos são disjuntos, nada garante que são independentes. A volta também é inválida |
|  2   |                                                                                 |     Se A e B são independetes, então A e $B^c$ também são indepedentes(e também $a^c$ eB, $A^c$ e $B^c$)                                                                                         |
	_Exemplo-1_ 
	![[diagram_1.svg]]
		P({.}) = $\frac{1}{4}$;     P($A \cap B$)= 1/4 
		$P(A \cap B) = P(A). P(B)= \frac{1}{4}$    $\begin{cases} P(A) = \frac{2}{4} = \frac{1}{2}\\ P(B) = \frac{2}{4} = \frac{1}{2}\end{cases}$
		Com isto, A e B são independentes 
		Analogamente, B e C são independentes e A e C são independentes, porém:
		$P(A \cap B \cap C) = \frac{1}{4} \neq P(A).P(B).P(C)=\frac{1}{8}$
		Logo A,B,C não são coletivamente independentes
	Demonstração 2:
		![[diagram2.svg]]
		Note que $A = (A \cap B) \cup (A \cap B^c)$; são disjuntos
		$P(A) = P((A \cap B) \cup (A\cap B^c)) \xrightarrow {disjuntos} P(A \cap B) + P(A \cap B^c) \rightarrow$
		$P(A)P(B)+ P(A \cap B^c) \Rightarrow P(A \cap B^c) = P(A)-P(B).P(A)= P(A)(1-P(B))= P(A).P(B^c) \Rightarrow P(A \cap B^c) P(A)P(B^c)$
		Logo, 
		