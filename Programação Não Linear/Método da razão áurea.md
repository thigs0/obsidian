Dado o método com busca exata, tentamos escolher 
$$\begin{align} \alpha=\arg \min f(x_k+\alpha d_k)\\ x_{k+1}=x_k+\alpha_k d_k\end{align}$$
- Como avaliar a derivada para encontrar este [[Minimizador]] pode ser caro em várias iterações. Tentamos encontrar ele apenas avaliando a função.

Como a função é de descida, criamos uma $\phi (\alpha)$ e tentamos encontrar o mínimo dela em um intervalo [a, b]
![[curva_ab.png]]
temos $f(a)$ e $f(b)$, escolhemos dois pontos $c$ e $d$ tal que $a< c <b, a<d<b, d\neq c$ 
Desde modo agora temos quatro pontos e avaliamos qual dos 3 formam uma concavidade, que possa indicar um mínimo para avaliar descartar a ou b.
![[curva_abcd.png]]
Neste caso são [a,c,d]
Então Descartamos b e realizamos este processo até $|a_k-b_k |\leq \epsilon$

###### Algoritmo
Dado $a,b \in \mathbb{R}$ 
escolha $c,d\in \mathbb{R}; a<c<d<b$ 
**While** $|a-b|<\epsilon$
	**Se** $f(c)>f(d)$
	 $\begin{align} a=a\\ b=d\\c=c\end{align}$
	**Se não**
	 $\begin{align} a=c\\ b=b\\ c=d \end{align}$

```julia
function min_rand(f::Function, a::Int64, b::Int64, ε::Int64)
	if a > b # Deixa a,b em ordem crescente
		a,b = b,a;
	end
	c = a + (b-a)*rand() #Gera os números aleatórios
	d = a + (b-a)*rand()

	if c > d # se c é maior que d, ordenamos
		c,d = d,c;
	end

	while abs(a-b) > ε # se a distância é maior queε  a solução não é boa
		d = a + (b-a)*rand();
		if f(c) > f(d)
			a,b,c = a,d,c;
		else
			a,b,c = c,b,d;
		end
	end
	return c;
end
```

Essa função diminui com distância aleatória, queremos agora em cada iteração eliminar pelo menos uma porcentagem do intervalo.
Assim, escolhemos $c,d$ de modo que
$$\frac{b-d}{b-a}=\frac{c-a}{b-a}=\frac{d-c}{d-a}=\frac{d-c}{b-c}$$
assim, temos 
$c = a+\gamma (b-a)$
$d=b-\gamma (b-a)$ => $\gamma^2-\gamma +1=0$ então $\displaystyle \gamma =\frac{3-\sqrt{5}}{2}$ 
