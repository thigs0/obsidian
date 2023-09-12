Ambos tentam melhorar o [[Método de Newton]]
- # [[Método das cordas]]

$\displaystyle x_{k+1}=x_k-f(x_k)/f'(x_0)$; A diferença para o método de newton é que tomamos a [[Derivada]] em um ponto fixo e inicial

- ### Algoritmo
```octave
function xn = cordas(x0, f, df, tam)
	while f(x0) > tam
		x0 = x0- f(x)/df;
	endwhile
	xn= x0
endfunction
```
```julia
function cordas(x0, f, df, tam)
	while f(x0) > tam
		x0 = x0-f(x)/df
	end
return x0
```
- # [[Método da secante]]

$\displaystyle g_k = \frac{f(x_k)-f(x_{k-1})}{x_{k}-x_{k-1}}$; usamos a definição de derivada para aproximar a derivada

- Precisa de dois pontos iniciais

```octave
function xn = secante(x0, x1, f, tam)
	while abs(x1-x0) > tam
		aprox = (f(x1) - f(x0))/(x1-x0);
		x0 = x1; x1 = x1 - f(x1)/aprox;
	endwhile
	xn=x0
endfunction
```
```julia
function secante(x0, x1,f, tam)
	while abs(x1-x0) > tam
		aprox = (f(x1) - f(x0))/(x1-x0);
		x0 = x1; x1=x1-f(x1)/aprox;
	end
return xn = x0
```