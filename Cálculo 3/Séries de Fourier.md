É uma ótima aproximação quando queremos considerar uma função periódica

**Definição**
	f(t) é periódica de período p se f(t+p) = f(t)

A série é de forma
$$\large f(t) = \frac{a_0}{2}+ \sum_{n=1}^\infty a_n cos(nt) + \sum_{n=1}^\infty b_n sen(nt)$$

podemos encontrar os $a_n$ com [[Integral]] definida

$\displaystyle a_n =  \frac{1}{L}\int_{-L}^L f(x)cos\left( \frac{n \pi x}{L} \right)$


$\displaystyle a_0 = \frac{1}{L}\int_{-L}^L f(x)dx$

e bn
$\displaystyle b_n = \frac{1}{L} \int_{-L}^L f(x)sen \left( \frac{n \pi x}{L}\right)$

