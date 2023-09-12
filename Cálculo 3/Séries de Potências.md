É definida como 
$\displaystyle \sum_{k=0}^\infty c_k(x-x_0)$

**Método de série de potência**
	Caso tenhamos uma equação por exemplo $x^2y'=y-x-1$
	supomos que y = $\displaystyle \sum_{k=0}\infty a_kx^k$-> $\displaystyle y1 = \sum_{k=1}^\infty a_kkx^{k-1}$
	$\displaystyle \sum_{k=1}^\infty a_kkx^{k+1} - \sum_{k=0}^\infty a_kx^k + x+1=0$; trocamos os k da primeira soma para k<- k-1
	$\displaystyle \sum_{k=2}^\infty a_{k-1}(k-1)x^k - \sum_{k=0}^\infty a_kx^k +x+1=0$; em k=1 temos 0, então podemos começar em 1
	$\displaystyle \sum_{k=1}^\infty (a_{k-1}(k-1)-a_k)x^k -a_0~~+x+1=0$
	os termos constantes são 0
	$a_0+1=0$
	os termos de x
	$-a_1x+x=0$
	a partir deste passo temos 
	$a_{k-1}(k-1)- a_k=0$
	
**Definição:**
	Dizemos que x=a é ponto ordinário para equação $y'' +P(x)y'+Q(x)y =0$. Se P(e) e Q(xx) forem analítcas em x=a; caso contrário dizemos que x=a é um ponto singular
	_Exemplo_
	$(x^2-3)y'' +2xy'=0$ -> $\displaystyle ny'' + \frac{2x}{x^-3}y'=0$
	P(x) é analítico em x=0
	Q(x) é analítico em x=0
	Então x=0 é um ponto ordinário da equação

**[[Teorema do ponto ordinário]]**
	Dada a equação na forma $y'' +p(x)y' +q(x)y =0$ e suponha que x=a é ponto ordinário. Então
	1) Existem duas soluções [[Linear independente]] dada por [[Série geométricas]] na forma $\displaystyle \sum_{k=0}^\infty C_k (x-a)^k$ com raio mínimo de convergência $r_{\text{mínimo}}=d(a,\text{Ponto singular mais próximo})$

X=0 é ponto singular regular se P(x) e q(x) são analíticas em x=0
_Exemplos_:
	Euler-Cauchy é singular regular

**[[Série de Frobenius]]**
	$\displaystyle \large y(x) = x^r\sum_{k=0}^\infty c_kx^k = \sum_{k=0}^\infty c_k x^{k+r}$; $c_0 \neq 0$
	Frobenius supôe que em uma equação de ponto singular regular, a solução é de modo acima
**[[Teorema de Frobenius]]**
	Se x=0 é ponto singular regular para a equação $x^2y''+xp(x)y'+q(x)y=0$ e $r_2 \geq r_2$ raízes da equação indicial. $r(r-1) +p(x)+ q(x)= 0$
	Então se $r_1 - r_2 \notin \mathbb{Z}^+$, temos duas soluções de frobenius [[Linear independente]]
	de forma:
	$\displaystyle \large \sum_{0}^\infty a_kx^{k+r_1}$ e $\displaystyle \large \sum_0^\infty b_k x^{k+r_2}$ 
	Para a maior raíz, sempre existe solução e o raio de convergência é pelo menos o $\displaystyle \large min\{r_{p(x)}, r_{q(x)}\}$
	_Exemplo_
	$2x^2y'' + xy' - (1+2x^2)y = 0$ --> Analisando, temos singularidade em x=0
	
	
