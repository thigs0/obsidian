## Integração numérica ou Quadratura
- Sabendo a função $\Psi(x)$, queremos aproximar a  $\displaystyle \int \Phi(x)$ 
- Convergência lenta
Podemos dividir o eixo x em pontos equidistantes por $h$ e entre dois pontos da absissas, traçamos uma retas. Assim, podemos aproximar a área da função como a área em baixo desta linha que forma um trapézio


![[integracao_h.png]]

Contruímos uma função qualquer, traçando uma reta entre os pontos f(a) e f(b). Temos um trapézio, de área e a quadratura do trapézio:
$$\int^a_b f(x) \approx A_{trapezio} = \frac{(f(a)+f(b))*(b-a)}{2}= \frac{f(a)+f(b)}{2}*h$$

Usando esta lógica para a função inteira, obtemos:
![[sequencia_h.png]]

E assim, temos os termos em sequência:
$$\int f(x) \approx \frac{f(a)+f(b)}{2}h+\frac{f(b)+f(c)}{2}h+\frac{f(c)+f(d)}{2}h+\frac{f(d)+f(e)}{2}h+\frac{f(e)+f(f)}{2}h$$
Generalizando, $\displaystyle \sum_{x=x_1}^{x_n} \frac{f(x_0)+f(x_1)}{2}h$  = h$\displaystyle \left( \frac{f(x_0)}{2} + f(x_1) + f(x_2) + f(x_3) + ... + f(x_{n-1}) + \frac{f(x_n)}{2}\right)h$ ; Considerando uma subdivisão $h$ contínua


- ## Erro
	o erro herda as propriedades do erro da [[interpolação]]. Assim o [[Erro]] da [[integral]] será:
	$\displaystyle \large Erro = \int_a^b \frac{f''(\epsilon_x)}{2!}(x-a)(x-b)dx = \frac{f''(\epsilon_x)}{2}\int_a^b (x-a)(x-b)dx = - \frac{(b-a)^3}{12}f''(\epsilon)$;        $\displaystyle \large \epsilon \in (a,b)$  

	O erro da composta é a soma das erros de cada intervalo $\displaystyle =-\frac{3h^3}{12}\left[ \frac{f''(\epsilon_1)+f''(\epsilon_2)+f''(\epsilon_3)}{3} \right]$, pelo [[Teorema do valor médio]], podemos representar aquela média por um ponto do intervalo 
	Isto é:
	Erro<$\displaystyle \frac{(b-a)h^2}{12}M_2$, em que $M_2$ é o máximo da derivada segunda da função

**Exemplo:**
 Aproximar a função $\displaystyle \int_1^4 \frac{1}{x}e^{x/2} dx$ representada abaixo, usando 3 intervalos

```functionplot
---
title: Função que aproximaremos a integral
disableZoom: false
bounds: [1, 4, 1.3, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = (2.7182^(x/2))/x

```


```octave
f = @(x) (e^(x/2))/x # função definida
x0 = 1; xn=4; n= 3; # Ponto inicial da malha, Ponto final, Tamanho do intervalo
area = 0 # Armazenará o valor da área
h = (xn-x0)/n

for x = x0:h:xn
if x==x0 | x==xn
area += f(x)/2
else
area += f(x)
endif
endfor
area *= h
```
```julia
function trapezio(f, x0,xn, n)
	area=0;
	h=(xn-x0)/n #passo 
	# já adiciona os extremos
	area += f(x0)/2
	area += f(xn)/2
	
	for x in x0:h:xn-h
		area += f(x)
	end
	return area*h
end
```

## Método de Simpson - Quadratura de simpson
- Aproximamos a integral por um polinômio interpolador de grau 2
- Para cada intervalo, usamos o ponto médio dele
- área abaixo do polinômio interpolador $p_2$ dados a,b e m, chamando h da distância de a até o ponto médio
A integral do polinômio interpolador deve aproximar a área
 $$\int_a^b f(a)\frac{(x-m)(x-b)}{(a-m)(a-b)}+ f(m)\frac{(x-a)(x-b)}{(m-a)(m-b)}+f(b)\frac{(x-a)(x-m)}{(b-a)(b-m)}$$                


Aplicamos [[Polinômio de Lagrange]] para $P_2$


Dado um intervalo -> [a,b]
com ponto médio -> m

O polinômio interpolador é 
$$f(x) \approx P_2(x) = f(a)+\frac{(x-a)}{h}\left( f(m)-f(a)+\frac{(f(b)-2f(m)+f(a))}{2h}(x-m)\right)$$
Então
$$\int_a^b f(x)dx \approx \int_a^b p_2(x)dx=\frac{h}{3}(f(a)+4f(m)+f(b)) = Q_S[f]$$


Se quisermos mais subintervalos, dividimos sempre de dois em dois e aplicamos a aproximação acima

	$$Q_S = \frac{h}{3}(f(x_0)+4f(x_1)+2f(x_2)+4f(x_3)+...+2f(x_{n-2})+4f(x_{n-1})+f(x_n))$$
## **Erro**
- integramos o erro da aproximação do polinômio

$\displaystyle Erro =- \frac{1}{90}(\frac{(b-a)}{2})^5 f^{(4)}(\psi)$; Demonstração usa [[Núcleo de Peano]], serve para grau 3
**Na forma composta**
$\displaystyle -\frac{n}{2}\frac{h^5}{90}$ --> $\displaystyle \frac{(b-a)h^4}{180}f^{(4)}(\psi)$
	**Demonstração**
	

- ## ==Condições de funcionamento==
	- $\displaystyle n$ precisa ser par
	- Os pontos são igualmente espaçados


- ### Algoritmos
	- **Pseudo código**
		$x_0$ <-- a                 # ponto inicial
		$x_n$ <-- b                 # Ponto final
		h <-- Intervalo que queremos
		x <-- vetor de pontos de espaçamento h de $x_0$ até $x_n$ 
		$f(x)=...$ # E a função f que queremos aproximar 
		y <-- f(x) # a função nos pontos de x
		A <-- 0                   # armazenamos a área
		Para i de 0 até n 
			Se i== 0 | i== n
				A <- A + f($x_i$)
			Se não $i~\%~2==0$ # Se i for par
				A <-- A + $\displaystyle 2*f(x_i$)
			Caso não          # i é ímpar
				A <-- A+ $\displaystyle 4*f(x_i)$
		A <-- A*(h/3)
	- **Octave**
	 ```octave
x0 = 1; xn = 2; h=1; # Ponto inicial e final, e o intervalo pedido
f = @(x) (e.^x)./x ;# Função que queremos aproximar a integral
x = x0:h:xn;   # Pontos com espaçamento h de x0 até xn
A = 0;         # Armazenamos o valor apróximado da área
y = f(x);      # Valor de y nos pontos de x
for i=1:length(x);
if (i == 1) | (i == length(x)); # Se é o primeiro ou último ponto
A += y(i);
elseif rem(i,2) == 0 # Se o resto da divisão é 0
A += 4*y(i);
else
A += 2*y(i);
endif
endfor
A = A*(h/3)
	 
	 ```
	- **Interno octave**
	```octave
	f = @(x)  #função para aproximar
	x0 = 0 # Ponto inicial
	xn = 3 #Ponto final
	A = quad(f,x0,xn) #Processo interno do octave para cálcular quadratura
	
	```
	- Julia
```julia
function simpson(f, x0, xn, n)
"""
f: is the function to integrate
x0: is the initial x point
xn: is the end x point
n: number point 
"""

h=(xn-x0)/(n-1) #step
area = f(x0)+f(xn) # add initial and end point
x = Vector(x0:h:xn) # 
apoio=2:length(x)-1

for i in apoio

	if rem(i, 2) == 1
		area += 2*f(x[i])
	else
		area += 4*f(x[i])
	end 
	
end
return area*(h/3)
end
```