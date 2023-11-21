#### Exemplo do método de Newton
**Hipóteses**
- Seja $x_0$ uma aproximação razoável para $x_*$, onde f($x_*$)=0
- f tem segunda [[Derivada]] contínua
- f($x_*$)=0 e f'($x_*$)$\neq 0$ 

--> Termo principal:  $\displaystyle x_{k+1} = x_{k}-\frac{f(x_k)}{f'(x_k)}$ 

-> Se $x_0$ não for razoável, podemos usar outro método para melhorar e depois aplicar Newton
-> Se a derivada deu 0, usamos o ponto do início


- Podemos deixar $\epsilon$ como $|f(x_k)|<\epsilon$ ou $\displaystyle \frac{|f(x_k)|}{|f'(x_k)|}< \epsilon$ 
- **Convergência** 
	$\displaystyle \lim_{k \to \infty } \frac{|e_{k+1}|}{|e_k|^2} = C$ ; Convergência quadrática

- #### Algoritmo:
	- #### Pseudo-Código
		f <- Recebe a função que queremos encontrar a raiz
		df <- Recebe a derivada da função f
		x <- Aproximação inicial
		- **Enquanto**  |$\delta$| > critério de parada
			x = x - f(x)/df(x)
	

	```octave
	function x = newton(f,df,x0)
	%% f é função que queremos minimizar
	% df derivada que queremos minimizar
	%xo é a aproximação inicial
	cont=0;x = x0;
		while abs(f(x)) > 10^-16 && cont<100
			x = x - f(x)/df(x);
			cont+=1;
		endwhile
	endfunction
	```
```julia
function newton(f::Function,df::Function,x0::Float64)
	#= f é função que queremos minimizar
	   df derivada que queremos minimizar
	   x0 é a aproximação inicial=#
	cont=0;x = x0;
	while (abs(f(x)) > 1e-16) && (cont < 300)
		x = x - f(x)/df(x);
		cont+=1;
	end
	return x
end
```

Exemplo:
```octave
 f = @(x) x.^2 + 2*x - sin(2*x-1);   # função f
 g = @(x) 2*(x+1) - 2*cos(2*x-1);    # derivada de f
 x = 0;                              # aproximação inicial
f(x)                                # valor de f no ponto inicial
ans =  0.84147
> x = x - f(x)/g(x), f(x)             # 1ª iteração de Newton e valor de f
x = -0.91524
ans = -0.68671
> x = x - f(x)/g(x), f(x)             # 2ª iteração de Newton e valor de f
x = -0.58406
ans = -0.00015520
> x = x - f(x)/g(x), f(x)             # 3ª iteração de Newton e valor de f
x = -0.58398
ans = -0.0000000041128
> x = x - f(x)/g(x), f(x)             # 4ª iteração de Newton e valor de f
x = -0.58398
ans =   -2.2204e-16
```
```functionplot
---
title: Graph
disableZoom: false
bounds: [-10, 10, -10, 10]
grid: true
xLabel: x
yLabel: y
---

f(x) = x^2
g(x) = 0.5*x^3+x^2-44
```

