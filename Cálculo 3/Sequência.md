**Para sequências infinitas**
$\large f: \mathbb{Z^+} \rightarrow~~ \mathbb{R}$ 
F(n) = $a_n$ tal que n é o índice da sequência

**Definição**
	Uma sequência $(a_n)$ converge para L quando é o [[Limite]] de n vai ao infinito $$\large a_n \Rightarrow \lim_{n \to \infty} a_n = L$$
	e converge se dado qualquer $\epsilon >0$ existe um $N \geq 0$ tal que $|a_n-L|< \epsilon$ para todo $n \geq N$
*exemplo*
$\displaystyle \frac{n-1}{n} \rightarrow 1$ dado um $\epsilon >0$. Existe N t.q
$\displaystyle \left| \frac{n-1}{n}-1\right| < \epsilon$ 
$\displaystyle \left| \frac{1}{n}\right| < \epsilon$ -> n > $1/\epsilon$. basta tomar N como n

- Toda sequência convergênte é limitada
	$|a_k| <k$

**Uma sequência que não converge é dita que [[diverge]]** 
	Uma sequência $a_n$ -> $\infty$ se dado qualquer k>0 existe para todo $n \geq N$ 
	*Exemplo*:
	$n^2$ e $(-1)^n$ 

**Propriedades**
	Se $a_n$ -> L e $b_n$ -> M então:
	1) $a_n + b_n \rightarrow L+M$ 
	2) $a_n .b_n \rightarrow L.M$
		Prova: Usamos a [[Desigualdade triangular]] $|a_nb_n - a_nM +a_nM -LM| \leq |a_nb_n -a_nM|+ |a_nM-LM|$
		$|a_n||b_n-M|+|M||a_n-L| \leq \epsilon$
		escolho $\epsilon_2 = \epsilon /2K$ e $\epsilon = \epsilon/2|M|$ 
	3) $\displaystyle \large \frac{a_n}{b_n} \rightarrow \frac{L}{M}$ , quando $M \neq 0$ 
	4) $\large c.a_n \rightarrow c.L$ sendo c uma constante


**[[Sequência monôtona]]**
 É uma sequência em que ela sempre cresce de forma que
 $a_1 < a_2 <a_3<...a_n<a_{n+1}$
 e o comparativo pode ser $<, \leq , >, \geq$  e todos são monôtonas

**Teorema**:
	Toda [[Sequência monôtona]] e limitada é convergente
	Prova:
	Pelo [[Axioma da completude]], existe a menor cotas uperior L 
	$a_n \leq L$ Existe N tal que $L - \epsilon \leq a_N < a_n \leq L < L + \epsilon$ => $L-\epsilon < a_n < L + \epsilon$
	$|a_n-l| < \epsilon;~~n \geq N$

**Teorema**:
		Se f é [[Contínua]] em x=L e $a_n \rightarrow L$ então $f(a_n) \rightarrow f(L)$ 