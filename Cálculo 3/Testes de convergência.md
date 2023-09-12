[[Teste da integral]]
Se a [[Integral impropria]] converge, a versão discreta converge
$\displaystyle \int_1^\infty f(x)dx ~~converge ~~\Rightarrow \sum_{k=2}^\infty a_x~~converge$ se $\displaystyle \int_1^\infty f(x)dx ~~diverge ~~\Rightarrow \sum_{k=2}^\infty a_x~~diverge$ 
[[Teste da comparação]]
Supomos que $0 \leq a_k \leq b_k$ 
1) Se $\sum b_k$ converge -> $\sum a_k$ converge
2) Se $\sum a_k$ diverge -> $\sum b_k$ diverge 
*Exemplos*
	$\displaystyle \sum \frac{\sqrt{k}-1}{k^2+1}$ , comparamos usando a desigualdade
	$\displaystyle 0 \leq \frac{\sqrt{k}-1}{k^2+1} \leq \frac{\sqrt{k}}{k^2}= \frac{1}{k^{3/2}}$ 
	Como o limitante superior é uma [[Série P]] e converge, o nosso termo também converge 

**[[Teste limite-comparação]]**
	$a_k >0$ e $b_k > 0$
 Se $\displaystyle \lim_{k \to \infty} \frac{a_k}{b_k} = \rho$ e $\rho \neq 0$ e $\rho \neq \infty$ 
 então ambas as séries têm o mesmo comportamento
**[[Teste da razão]]**
	Sejam $a_k > 0$ 
	Se $\displaystyle \lim_{k \to \infty} \frac{a_{k+1}}{a_k} =L$
	então
	1. Se L<1 -> $\sum a_k$ converge
	2. Se L>1 -> $\sum a_k$ diverge
	3. Se L=1 -> nada podemos afirmar
**[[Teste da raíz]]**
	Consideramos $a_k>0$ 
	Se $\displaystyle \lim_{k \to \infty} (a_k)^{1/2} =L$ Então,
	1. Se L<1 -> $\sum a_k$ converge
	2. Se L>1 -> $\sum a_k$ diverge
	3. Se L=1 -> nada podemos afirmar
**[[Teste das séries alternadas]]**
	Se $a_k$ descrece
	Se $\displaystyle \lim_{k \to \infty} a_k =0$ 
	Então $\displaystyle \sum_{k \to \infty} (-1)^ka_k$ converge