- ##### O princípio básico da contagem
	 Suponha a realização de dois experimentos. Se o experimento 1 pode gerar qualquer um de m resultados possíveis e se, para cada um dos resultados do experimento 1, houver n resultados possíveis para o experimento 2, então os dois experimentos possuem conjuntamente mn diferentes resultados possíveis.

[[Combinação]]
$$C_{n,r}= \begin{pmatrix} n \\ r\end{pmatrix}= \frac{n!}{(n-r)!r!}$$
```julia
function C(n, r)
	x=factorial(n)/(factorial(n-r)*factorial(r))
	return x
end
```
Teorema binomial
$$\displaystyle (x+y)^n = \sum_{k=0}^n \begin{pmatrix} n \\ r\end{pmatrix} x^ky^{n-k}$$

**[[Distribuição normal]]** ou **[[Gaussiana]]**
	É distribuição mais importante para uso em análise estatística
	É uma aproximação para a distribuição binomial
	$$\Large DP_{n_1}= \frac{1}{\sigma \sqrt{2\pi}}e^{-\frac{(n_1-m)^2}{2\sigma^2}}d_{n_1}$$
	$\sigma$ é o desvio padrão (Largura da distribuição para o valor médio)
	$m$ é o valor médio verdadeiro
	$\displaystyle \bar{n_1} = \frac{1}{n}\sum_1^n n_1$

**[[Distribuição de Poisson]]**
	Para P muito pequeno que 1
	Para N muito maior que 1
	$\displaystyle \large P_{n_1} = \frac{m^{n_1}}{n_1!}e^{-m}$
#### Avaliação de incertezas
A) Avaliação da incerteza via análise estatística




