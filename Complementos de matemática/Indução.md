O princípio da indução é usado para provar uma regra valida para n números quaisquer

(i) A(1) é verdadeira
(ii) A(k) é verdadeira

_Exemplo_:
prove que para todo natural n $\displaystyle 1+2+3+4+...+n= \frac{n(n+1)}{2}$

i) Provar para n=1
1= $\displaystyle \frac{1(1+1)}{2}=1$ 

ii) Supor verdadeira para k e provar para k+1
$1+2+3+4+...+k = \frac{k(k+1)}{2}$ é válida
para K+1
1+2+3+4+...+k+(k+1) = $\frac{(k+1)(k+1+1)}{2}= \frac{(k+1)(k+2)}{2}$
distribuimos
$\frac{k(k+1)}{2}+ \frac{2(k+1)}{2}= \frac{k(k+1)}{2} + k+1$
Como é válido para k, observamos que os dois lados são iguais



**Exercícios**
1) Prove que $1.2 + 2.3 + 3.4+ 4.5+...+n(n+1)= \displaystyle \frac{n(n+1)(n+2)}{3}$
	Verificamos para n=1
	$1(1+2)=1.2=2$,  $\displaystyle \frac{1(1+1)(1+2)}{3}=2$. Então para n=1 verificamos que a igualdade é válida 
	supomos que tenha um n que a igualdade também seja válida, para n+1 temos
	$\displaystyle \frac{(n+1)(n+2)(n+3)}{3}$ = $\displaystyle \frac{n(n+1)(n+2)}{3}+\frac{3(n+1)(n+2)}{3}= \frac{n(n+1)(n+2)}{3}+(n+1)(n+2)$ .
	Como para n é válido, temos que para n+1 também é válido 
1) Prove que $\displaystyle \frac{1}{1.2} + \frac{1}{2.3}+ \frac{1}{3.4}+...+\frac{1}{n(n+1)} = \frac{n}{n+1}$ 
	Verificamos para n=1
	$\frac{1}{1(1+1)}=\frac{1}{2}$ e $\frac{1}{1+1}=\frac{1}{2}$. Então é válido para n=1
	Supondo válida para um certo n, n+1
	$\frac{n+1}{n+2}$ = $\frac{n}{n+2}+\frac{1}{n+2}$
1) Prove que $1^2 + 2^2+3^2 + ...+n^2  \leq n^3$
	Para n=1,
	$1^2=1$ e $1^3=1$, então para n=1 é válido
	se for válido para um n, n+1
	$(n+1)^3=n^3+3n^2+3n+1$, como$\sum n^2\leq n^3$=>
	$n^3+3n^2+3n+1 \geq \sum n^2 +3n^2+3n+1$ =$\sum n^{2}+ (n+1)^2+2n^2+n$=>$(n+1)^3\geq \sum (n+1)^2$  