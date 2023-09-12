- Um dos testes de tendência mais usados para séries temporais
- Usado pela Organização Meteorológica Mundial (OMM)
As hipóteses são:
1. Não há tendência presente nos dados
2. Uma tendência está presente nos dados que pode ser de aumento ou de diminuição

Usamos também o teste estatístico parametrizado (ZMK)

| Estatística S | Valor p | Tendência     |
| ------------- | ------- | ------------- |
| s >0          | p < 0.05 | Crescimento   |
| s > 0           | p > 0.05  | Sem tendência |
| s = 0           | -       | Sem tendência |
| s < 0           | s > 0.05  | Sem tendência |
| s < 0           | p < 0.05  | Decrécimo              |

**Algoritmo**
função sgn(v)
	$\begin{cases}1~~ se~v>0\\0~~ se~v=0\\-1~~se~v<0\end{cases}$
end

x -> Dados 
n -> Quantidade de dados em x
s=0
**Para** i de 1 até n-1
	**Para** j de i+1 até n
		s += $sgn(x_j-x_i)$ 

```julia
function MK(x)
	function sgn(v) # Função auxiliar de apoio
		if (v>0)
			return 1;
		else if (v==0)
			return 0;
		else if (v<0)
			return -1;
		else
			error("The input value is not a number!")
	end
	
	s=0;
	n = length(x);
	for i in 1:n-1
		for j in i+1:n
			s += sgn(x[j]-x[i]);
		end
	end
	return s;
end
```


### [[Pre-Whitening]] PW
Caso apliquemos este teste.
seja n a quantidade de dados na nossa amostra
$$S =\sum_{i=1}^{n-1}\sum_{j=i+1}^n sgn(x_j-x_i)$$
que é a descrição do [[Teste Mann-Kendall]]
Então calculamos:$$V(S)=\frac{n(n-1)(2n+5)-\displaystyle\sum_{m=1}^n ti(m-1)(2m+5)}{18}$$
Por fim 
$\begin{cases}\displaystyle\frac{S-1}{\sqrt{V(s)}}~~Se~S~for~>0\\ 0~~Se~S~for~=0\\ \displaystyle \frac{S+1}{\sqrt{V(s)}}~~Se~S~for~<0\end{cases}$


### [[Trend-Free Pre-Whitening]]
Este método usa os mesmos do anterior e 
### [[Modified Trend-Free Pre-Whitening]]

Ambas as técnicas iniciam com a estimativa do lag-1 [[Auto-Correlação]] com [[Coeficiente de determinação]] da série original.
Caso este valor não seja alto, aplicaremos o teste normal
removemos os valores com maiores significâncias da série original

**Referência**
![Artigo do Professor Blain](https://www.scielo.br/j/rbmet/a/KK9qRdWGMN3HKjmQhbrWpZr/?format=pdf)