*Forma padrão*
 $\min f(x)=c^tx$
 $s.a:~\begin{cases}Ax=b\\ x\geq 0\end{cases}$ 
 - Uma [[função]] linear chamada função objetivo
 - Dados $a_{ij}$ e $b_i$, $i=1,2...,m,~~j=1,...,n$ 
 - as incógnitas são chamadas de variáveis
**Definição**
Uma solução é factível se atende todas as restrições do problema 

**Definição**
O conjunto de todas as soluções factíveis define uma região no $\mathbb{R}^n$ chamada região de factibilidade

**Definição** 
Uma solução é ótima se é factível e fornece o menor valor para a função objetivo f. Isto é uma solução factível ($x_1^*,x_2^*,...,x_n^*$) for tal que 
$$f(x_1^*,x_2^*,...x_n^n)\leq f(x_1,x_2x,...,x_n)$$
para qualquer solução factível, então temos uma solução ótima
1. ***Problema de Maximização***
	maximizar f(x) corresponde ao mesmo que minimizar -f(x)
	Assim, passamos os temos para a forma de minimização
2. ***Restrição de desigualdade***
	$\displaystyle \sum_{i=1}^n a_{i1}x_1 \leq b_i$
	$\displaystyle \sum_{i=1}^n a_{i1}x_1 + \underbrace{x_k}_{\text{Variável de folga}} \leq b_i$
	com $x_k\geq 0;~k\geq (n+1)$ 
	**Exemplo**
	$\min f(x_1,x_2,x_3)=2x_1-3x_2+3x_3$
	$s.a: \begin{cases}x_1+2x_2-x_3\geq 3\\ -2x_1+x_2+x_3\leq -1\\ x_1\geq 0,x_2\geq 0,x_3\geq 0\end{cases}$ 
	Introduzimos as variáveis de folga, temos:
	$\min f(x_1,x_2,x_3,x_4,x_5)=2x_1-3x_3+3x_3$
	$s.a: \begin{cases}x_1+2x_2-x_3-x_4=3\\ -2x_1+x_2+x_3+x_5=-1\\ x_1\geq 0,x_2\geq 0,x_3\geq 0,x_4\geq 0, x_5\geq 0\end{cases}$
3. ***Variáveis Livres***
	$x_i$ irrestrita
	$$x_i=x_i^+-x_i^-,\text{com}~x_i^+\geq 0,~x_i^-\geq 0$$
	qualquer número pode ser sempre escrito como uma diferença de dois outros não negativos

###### Hipóteses
- O número de variáveis seja maior que o número de restrições (n > m, em geral, n é muito maior que m)
- o [[Posto]] de A

###### Geometria da otimização linear
**Teorema**
A região factível de um problema de programação linear é um [[Conjunto convexo]]

**Teorema**
Se o problema de otimização linear tem uma solução ótima, então existe um vértice ótimo


Quando construímos o problema, conseguimos observar que nos vértices as variáveis de folgas zeram em duas equações. Quando isso ocorre, conseguimos obter um sistema linear

**[[Ponto extremo]]**
x é um ponto extremo de S (conjunto de soluções factíveis) se possuir n-m variáveis nulas
