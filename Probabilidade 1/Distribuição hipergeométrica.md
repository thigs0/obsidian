Suponha que uma amostra de tamanho n seja obtida aleatoriamente **(Sem reposição)** de uma urna contendo N bolas das quais m são brancas e N-m são pretas.
	Retiramos n bolas
	X: # bolas brancas sorteadas na amostra
	$\displaystyle \large p(x) = P(X=x) = \frac{\begin{pmatrix}m \\ x \end{pmatrix} . \begin{pmatrix} n-m \\ n-x \end{pmatrix}}{\begin{pmatrix} N \\ n \end{pmatrix}}$; $n-(N-m) \leq x \leq min\{n,m\}$ 
	**A população precisa ter duas características**
	1. Uma população com duas características
	2. A distribuição conta o número de índivíduos

Dizemos que x tem distribuição hipergeométrica com parâmetro N,m e n e escrevemos x~HiperGeo(N, m, n)

*Exemplo* 
	Uma caixa com 25 peças, das quais 4 são defeituosas. Selecionamos sem reposição 5 peças; descartamos a caixa se tiver mais do que 2 peças defeituosas na amostra. Qual a probabilidade de ter uma caixa descartada
	X: # de peças defeituosas em uma amostra
	x ~ HiperGeo(25, 4, 5) = $\displaystyle P(X=x) = \frac{\begin{pmatrix}4 \\ x \end{pmatrix} . \begin{pmatrix} 25-4 \\ 5-x \end{pmatrix}}{\begin{pmatrix} 25 \\ 5 \end{pmatrix}}$

**Esperança**
	E(x) = $\displaystyle \frac{m.n}{N}$
**Variância**
	$\displaystyle Var(x)=~\frac{m.n}{N}\left[ \frac{(n-1)(m-1)}{N-1}- \frac{m.n}{N}+1\right]$
	