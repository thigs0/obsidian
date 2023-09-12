- Usamos o [[Polinômio de Taylor]]
- o método é chamado de [[Diferenças finitas]]
- Teremos uma no formato [[Matriz banda]]

- Aproximamos qualquer derivada pela fórmula
$$\displaystyle \large f^{(n)}(a)= \lim_{h \to 0} \sum_{j=0}^n \frac{(-1)^{n-j} \begin{pmatrix} n \\ n-j\end{pmatrix}f(a+jt)}{t^n}$$

### Método de diferenças finitas
A forma geral deste problema é $$\begin{cases} y''(x) = f(x,~ y(x),~y'(x))\\
y(a) = \alpha\\
y(b) = \beta\end{cases}$$
- Defina a malha $x_0<x_1<x_2<...<x_n$ ; onde $h = x_{i+1}-x_i$

- y sendo uma função suficientemente derivável, temos:
	$y(x_{i+1}) = y(x_i +h)= y(x_i) + hy'(x_i)+\frac{h^2}{2}y''(\epsilon) \Rightarrow$
	$$Y'(x_i) = \frac{y(x_{i+1})-y(x_i)-h^2y''(\epsilon)/2}{h}$$ e aproximamos para $$\begin{equation}y''(x_0) \approx \frac{y(x_{i+1})-y(x_i)}{h}\end{equation}$$
	Esta é a diferença avançada por olharmos o ponto e o próximo a ele.
	Se fosse o ponto e o anterior, se chamaria diferença atrasada

	Se subtratirmos a diferença avançada da atrasada, obtemos
	$\displaystyle y(x_{i+1})-y(x_{i-1}) = 2hy'(x_i) + \frac{h^3}{3!}(y'''(\sigma)+y'''(\sigma))$ ; o termo de h³ é analisado como duas vezes um y''' médio, isolamos o y' e obtemos

	$$y'(x_i) = \frac{y(x_{i+1})-y(x_{i-1})}{2h}$$e é chamada de diferença centrada e é melhor do que as últimas duas citadas


	- ###### Exemplo:
		- Aproxime Sin'(1),

		Diferença avançada -> $\displaystyle y'(x_i) = \frac{y_{i+1}-y_i}{h} = \frac{sin(1.1)-sin(1)}{0.1}= 0.49736$
		Diferença atrasada --> $\displaystyle y'(i) = \frac{y_{i}-y_{i-1}}{h} = \frac{sin(1)-sin(0.9)}{0.1} = 0.58149$
		Diferença centrada --> $\displaystyle y'(x_i) = \frac{y_{j+1}-y_{j-1}}{2h}= \frac{sin(1.1)-sin(0.9)}{2(0.1)} = 0.53940$
	- **[[Equação do calor]]** resolvido por diferença finita
		$\displaystyle \begin{cases} \displaystyle \frac{du}{dt}(t)=-\frac{\mu}{h^2}Au+f(t); \forall t >0 ~~e~~ A\text{ é uma matriz diagonal}\\ u(0) = u_0\end{cases}$
		
		```octave
		function [x,u] = heattheta(xspan,tspan,nstep,theta,mu,u0,g,f,varargin)
		
		h = (xspan(2)-xspan(1))/nstep
		dt = (tspan(2)-tspan(2))/nstep
		N = nstep(1)+1
		e = ones(N,1);
		D = spdiags([-e 2*e -e], [-1 0 1], N,N)
		I = speye(N)
		A = I+mu*
		
		```
##### Código em octave
```octave
    #Função que calcula a diferença avançada
function x = dif_avancada(funcao , inicio , passo)
	x = (funcao(inicio+passo)-funcao(inicio))/passo;
  return x
  
	# Função que calcula a diferença atrasada
function x = dif_atrasada(funcao, inicio , passo)
	x = (funcao(inicio)-funcao(inicio-passo));
	return x

	# Função que calcula a diferença avançada
function x = dif_centrada(funcao, inicio , passo)
	x = (funcao(inicio+passo) - funcao(inicio-passo))/(2*passo);
	return x
	
f = @(x)  # definimos a função que queremos aproximar a derivada

```

### Uso de diferenças finitas
$y''(x) + p_j(x)y'(x) + q(x)y(x) = r(x)$; com isto aproximamos a [[Derivada]] por

$\displaystyle \frac{y_{j+1}-2y_j + y_{j-1}}{h^2} + p_j \frac{y_{j+1}-y_{j-1}}{2h} + q_jy_j= r_j$; com j= 0, 1, 2, ..., n
$\displaystyle y_{j+1} \left( 2+ hp_j\right) + y_j\left( 2h^2q-4\right)+y_{j-1}(2-h) = 2h^2r_j$  -->
$$y_{j+1}\left( 1+ \frac{h}{2}p_j \right) + y_j(h^2 q -2) + y_{j-1}\left( 1-\frac{h}{2} p_j \right) = h^2 r_j(x)$$

```octave
function pontos = aprox2(h,x0,xn,f)
# f retorna na forma vetorial
n = (xn-x0)/h +1;# quantidade de pontos
vec = x0:h:xn; # cria p vetor igualmente espaçado

m = zeros(n-2, n-2); # Cria a matriz de zeros

for i = 2:n-1 # ignora o primiero e o último
X = vec(i);
if i == 2	#Início
	m(i-1,i-1) = f(X)(2);
	m(i-1, i) = f(X)(3);
elseif i != n-1 #  meio
m(i-1,i-2) = f(X)(1);
	m(i-1, i) = f(X)(3);
	m(i-1,i-1) = f(X)(2);
else  # Fim
	m(i-1,i-1) = f(X)(2);
	m(i-1,i-2) = f(X)(1);
endif
endfor

r = f(vec)(end,2:end-1)';

p = m\r(1:end);
pontos =[x0; p ; xn];
endfunction;

h= 0.2
x0 = 1
xn = 2
vec = x0:h:xn;
f = @(x) [1.+h./(6.*x); -h.^2./(6.*x.^2) ; 1.-h./(6.*x); (1.+x)./(3.*x.^2)];
f =@(x) [2.-x.*h ; h.^2.-4 ; 2.-x.*h ; e.^x.*x.*h.^2];
a = aprox2(h, x0, xn, f);
plot(vec,a)



```julia
function Diferenc_finit(malha, fa, y0, yn, X)
  """
  fa: is a vecyor function of (h, x)
    Exemple
    F(h, x) = [h+x x-h x+h^2] 
  X: is a function vectorial to the result matricial product
  """ 

  h = malha[2] - malha[1] #step size
  t = length(fa(1, 2))

  A = zeros(length(malha)-2, length(malha)-2)

  for i in 1:length(malha)-2

    if i == 1 # if is the first case 
      A[i, 1:t-1] = fa(h, malha[i+1])[2:end]'; # add the vector minus the first element
    
    elseif i==length(malha)-2 # if is the end caso

      A[i, end-(t-2):end] = fa(h, malha[i+1])[1:end-1];

    else
      # considering that the derivative is impar

      A[i, i-trunc(Int,(t-1)/2):i+trunc(Int, (t-1)/2)] = fa(h, malha[i+1])' 
     
    end
  end

  x0 = Vector{Float64}()
  for i in 1:length(malha)-2
    append!(x0, X(h, malha[i]))
  end

  # X is the vector result x os system
  X = x0
  
  X[end] -= yn; X[1] -= y0;

  x =  A\X
  
  #Add the inicial and final point
  
  t = zeros(length(malha))

  t[1] = y0; t[end] = yn;
  t[2:end-1] = x;

  return t
end

using Plots
malha = Vector{Float64}(0:0.01:1);

y0 = 2; yn = 0;
fa(h, x) = [1-2*h; 2+h; 2*h^2-4];
X(h, x) = x+0*h;

y = Diferenc_finit(malha, fa, y0, yn, X)
plot(malha, y)
savefig("olha.png")
```




