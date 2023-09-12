Este método tenta avaliar os melhores pontos, mesmo que eles não sejam igualmente espaçados como vêm ocorrendo para avaliar uma [[Integral]].
Vamos deixar tanto os pontos $x_i$ como os pesos $w_i$ como incógnitas e determinar de maneira conveniente

### Para um ponto
Queremos $\int_a^b f(x)dx \approx w_1f(x_1)$; com $x_1$ e $w_i$ tais que a fórmula seja exata para monômios de grau 0 e grau 1.
- Para ser exata em grau 0
	$\int_a^b 1dx = w_1f(x_1) \Rightarrow b-a = w_1$
- Para ser exata em grau 1
	$\displaystyle \int_a^b xdx =  w_1f(x_1) \Rightarrow \frac{x^2}{2}|_a^1= (b-a)x_1\Rightarrow \frac{b^a-a^2}{2}= (b-a)x_1 \Rightarrow x_1 = \frac{a+b}{2}$ 
Desta forma temos a fórmula 
	$\displaystyle I = (b-a)f\left( \frac{a+b}{2}\right)$ que integra exatamente um polinômio de grau $\leq 1$
_Exemplo_:
	Usar a fórmula da quadratura com um ponto para calcular $\ln 2= \int_{1}^2 \frac{1}{x}dx$ 
	a=1; b=2; $x_1 = \frac{a+b}{2}= 3/2$
	I = $(b-a)f(x_1) = 0.\bar{6}$ sendo que o exato é $0.69...$
```julia
function gaussiana1(f, b, a)
	# f: é a função dentro da integral
	# a: é o extremo direito
	# b: é o extremo esquerdo
return (b-a)*f((a+b)/2)
end
```
### Para dois pontos
Como dois pontos $x_1~e~x_2$ (e seus correspondente $w_1~e~w_2$) temos 4 incógnitas e portanto podemos exigir polinômio de grau até 3.
	usamos o intervalo de [-1, 1], e sempre mudamos as variáveis para recair neste intervalo
Queremos -> $\int_{-1}^1 f(t)dt \approx w_1f(x_1)+w_2f(x_2)$
- g(t) = 1 -> $\int_{-1}^1 dt= w_1 + w_2 \Rightarrow w_1+w_2=2$
- g(t) = t -> $\int_{-1}^1 tdt = w_1t_1 +w_2t_2 \Rightarrow w_1t_1+w_2t_2 =0$
- g(t) = $t^2$ -> $\int_{-1}^1 t^2dt = w_1t_1^2 + w_2t_2^2 \Rightarrow w_1t_1^2 +w_2t_2^2= 2/3$
- g(t) = $t^3$ -> $\int_{-1}^1 t^3dt = w_1t_1^3+w_2t_2^3 = 0$
Temos assim o [[Sistema não linear]] de 4 equações e 4 incógnitas
$\displaystyle \large \begin{cases} w_1+w_2 =2\\ w_1t_1+w_2t_2=0\\ w_1t_1^t +w_2t_2^2 = 2/3 \\ w_1t_1^3 +w_2t_2^3 = 0 \end{cases}$
De forma a termos $w_1=1$, $w_2 =1$ , $t_1= - \sqrt{3}/3$, $t_2= \sqrt3/3$

_Exemplo_:
	(1) Calcular Ln 2 = $\displaystyle \int_1^2 \frac{1}{x}dx$
	Mudamos a variável para $x=\frac{t+1}{2}+1$ e $dx = dt/2$
	-> $\displaystyle \int_{-1}^1 \frac{1}{\frac{t+1}{2}+1} \frac{dt}{2}$= $\int_{-1}^1 \frac{1}{t+3}dt$
	Assim;
	$\ln 2 \approx g(-\sqrt3/3)+g(\sqrt3/3) = 0.6923077$ erro na terceira casa decimal
	(2) Calcular $\displaystyle \int_0^{10} e^{-x}dx$
		Aplicando as mudanças de variável, temos: $x=5t+5$ e $dx = 5dt$
		$\int_{-1}^1 5e^{-5t+5}dt = g(-\sqrt3/3) + g(\sqrt{3}/3) = 0.6061$
```julia
function gaussiana2(f)
	return f(-sqrt(3)/3) + f(sqrt(3)/3)
```
### Para três pontos

| i   | $t_i$         | $w_i$ |
| --- | ------------- | ----- |
| 1   | $-\sqrt{3/5}$ | 5/9   |
| 2   | 0             | 8/9   |
| 3   | $\sqrt{3/5}$  | 5/9   |
|     |               |       |

**Fórmula do erro**
	Para quadratura gaussiana vista aqui como n pontos 
	$\displaystyle  \large E_n(f) = \frac{2^{n+1}(n!)^4}{(2n+1)[(2n)!]^2} \frac{f^{(2n)(\beta)}}{(2n)!}$
	Com $\beta \in (-1,~1)$ Isso integra até polinômios de grau $\leq 2n-1$ 
