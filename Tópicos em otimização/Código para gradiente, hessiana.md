- Geramos um código otimizado que calcule o [[Gradiente]], a [[Matriz Hessiana]] 

Entrada: $a,b,c \in \mathbb{R}$ 
Saída: Não podem ser os comprimentos do lado de um triângulo
ou
São os comprimentos dos lados de um triângulo com área

Coloca em ordem crescente a, b, c
x = a+b
**Define** Lei_cossenos como
	$t = -(a^2-b^2-c^2)/2bc$
	retorna t
**Define** Verifica(a, b, c)
	global A = (a+b)
	global B = (b+c)
	global C = (a+c)
	t = 0
	**se** A > c:
		t=1
	**se** B > a:
		t=1
	**Se** C > a
		t=1
	**Return** t
**Define** Area(a,b, c)
	s = $(A+c)/2$
	**Return** sqrt(s(s-a)(s-b)(s-c))
**Se** Verifica()
	t = b+c
	s = $(a+t)/2$ 
	m1 = Lei_cossenos(1 menor)
	m2 = Lei_cossenos(2 menor)
	m3 = 180-t
	**Retorna** são os comprimentos dos lados de um triângulo com área {Area(), perímetro {m1} {m2} {m3} e ângulos internos {arccos(m1)}, {arccos(m2)}, {arccos(m3)}	
**Else**
	**Return** "Não podem ser os comprimentos do lado de um triângulo"

$\displaystyle \frac{\partial f(x)}{\partial x_j}=\frac{f(x+he_j)-f(x-he_j)}{2h}+O(h^2)$
$\displaystyle \frac{\partial^2 f(x)}{\partial x_j^2}=\frac{f(x+he_j)-2f(x)+f(x+he_j)}{h^2}$
$\displaystyle \frac{\partial f(x)}{\partial x_jx_i}=\frac{f(x+he_i+he_j)-f(x+he_i-he_j)-f(x-he_i+he_j)+f(x-he_i-he_j)}{4h^2}+o(h^2),i\neq j$


```julia
using LinearAlgebra
function fun(x)
  n = length(x)
  if n<=0
    error("Fez merda")
  end
  return(x[1]^2+x[2]^2)
end

function grad(f, x, h)
  #f é a função
  #x é o ponto
  #h é o passo
  n = length(x)
  e = zeros(Float64, n) # elementar com zeros
  resul = zeros(Float64, n)
  for i in 1:n
    e[i] = 1.0;
    resul[i] = (f(x+h*e)-f(x-h*e))/(2*h);
    e[i] = 0.0;
  end
  return resul;
end

function hess(f, x, h)
  #x é o ponto 
  #h é o passo
  n = length(x)
  resul = zeros(n,n);
  ei = zeros(n)
  ej = zeros(n)
  c1 = h^2
  for i in 1:n
    for j in 1:n
      if (i != j)
        ei[i] = ej[j] = 1.0
        resul[i][j] = (f(x+h*ei+ej)-f(x+h*ei-h*ej)-f(x-h*ei+h*ej)+f(x-h*ei-h*ej))/(4*c1)
        ei[i] = ej[j] = 0.0
      else
        ei[i] = h
        println(resul[i][i])

        resul[i][i] = (f(x+ei)-2*f(x)+f(x+ei))/(c1)
        ei[i] = 0.0
      end
    end
  end
end
#testar

x = [2.0; 2.0]
r = grad(fun, x, 0.1)
println(r)
r = hess(fun, x, 0.1)
println(r)
```