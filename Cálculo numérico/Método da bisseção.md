- Seja a e b tais que $f(a)\cdot f(b)$ < 0 --> [[Teorema de Bolzano]]

- Demora:
	$\displaystyle \frac{L}{2^N}<\epsilon$ ; sendo menor do que um valor que  queiramos


- ### Algoritmo
```octave
	function ponto = bisse(a,b,f, tamanho)
	% a é o ponto positivo e b o ponto negativo
	cont=0;
	if f(a) < 0
	  temp = b;
	  b=a; a=temp;
	endif
	while abs(a-b) > tamanho && cont<100
		m = (a+b)/2; # ponto médio
		if f(m)>0
		a = m;
		else
		b = m;
	endif
	cont+=1;
	endwhile
	ponto = (a+b)/2;
	endfunction
```
**[[Julia]]**
```julia
function bisse(a,b,f::Function, tamanho::Float64)
	cont=0;
	while abs(a-b) > tamanho && cont <1000
	println(abs(a-b))
		m = (a-b)/2;
		if f(m) > 0
			a = m;
		else
			b = m
		end
		cont+=1
	end
	return a
end
```