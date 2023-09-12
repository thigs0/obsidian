Encontra uma função que passe pelos pontos
	Suponha que temos uma tabela de dados
	
| $x_0$ | $y_0$ |
| ----- | ----- |
| $x_1$ | $y_1$ |
| ... | ... |
|   $x_n$    |   $y_n$    |
e tentamos descrever os pontos por uma função simples computacionalmente
### [[Interpolação polinomial]]
Modelamos neste caso a função que aproxima os pontos de modo $$P(x) = a_0 +a_1x+a_2x^2+...+a_{n-1}x^{n-1}+a_nx^n$$
Com os dados, construímos $(n+1)_x (n+1)$ sistemas para se resolver
$$\begin{bmatrix}1 & x_0 & x_0^2 &...&x_0^n\\ 1 & x_1 & x_1^2 &...&x_1^n\\...&...&...&...&...\\ 1 & x_n & x_n^2 &...&x_n^n\\ \end{bmatrix} \begin{bmatrix} a_0 \\a_1\\..\\a_n\end{bmatrix}= \begin{bmatrix} y_0\\ y_1\\..\\y_n\end{bmatrix}$$

$\begin{bmatrix}1 & x_0 & x_0^2 &...&x_0^n\\ 1 & x_1 & x_1^2 &...&x_1^n\\...&...&...&...&...\\ 1 & x_n & x_n^2 &...&x_n^n\\ \end{bmatrix}$ Esta matriz é determinada [[Matriz de Vandermonde]]

| x   | y   |
| --- | --- |
| -1  | 6   |
| 2   | 3   |
| 3   | 10  |
Se $P(x) = a+bx+cx^2$
		- P(1) = a -1b +1c = 6
		- P(2) = a +2b +4c = 3  
		- P(3) = a +3b +9c = 10
		$$\begin{bmatrix}
		1 & -1 & 1 & |6\\
		1 & 2 & 4 &| 3\\
		1 & 3 & 9& | 10\\
		
	\end{bmatrix}$$
	Resolvendo o sistema, encontramos os índices
	- Se $P(x) =\alpha (x-2)+\beta(x+1) + \gamma (x+1)(x-2)$ 
		- $\alpha = -2$
		- $\beta = 1$
		- $\gamma = 2$

exemplo:
Dados os pontos:

| x   | y    |
| --- | ---- |
| 0   | -0.3 |
| 1   | 2.3  |
| 2   | 6.1  |

```functionplot
---
title: Gráfico da curva obtida do ajuste
disableZoom: false
bounds: [-4, 4, -6, 8]
grid: true
xLabel: x
yLabel: y
---

f(x) = -0.15*(x-1)*(x-2) - 2.3*x*(x-2) + 3.05*x*(x-1)

```
- ### Dado um problema de interpolação
	- Dado um problema de interpolação

	Seja $\Omega = {(x_0,y_0), (x,y),...,(x_n,y_n)}$ com $x_i < x_{i+1}$
	Quero determinar com polinômio P de grau máximo n, tal que $\displaystyle P(x_i) = y_i$; i=0, 1, ... ,n

	- ### Na base canônica:
		- $P(x) = a_0 + a_1x+a_2x^2 +...+a_nx^n$
	
		Construindo matricialmente
			$$\begin{bmatrix} 1 & x_0 & x_0^2 & ... & x_0^n\\
			1 & x_1 &x_1^2 & ... & x_1^n\\
			...&...&...&...&...\\
			1&x_n&x_n^2&...&x_n^n\\
			
			\end{bmatrix} . \begin{bmatrix} a_0\\
			a_1\\
			a_2\\
			...\\
			a_n\end{bmatrix} = \begin{bmatrix} y_0\\
			y_1\\
			y_2\\
			...\\
			y_n\end{bmatrix}$$
		 Se chama [[Matriz de Vandermonde]]		
		 e sua determinante é: $\displaystyle \det V(x_0,x_1,x_2,...x_n)= \prod_{i,j=0;~ i>j}^n (x_i-x_j)$

	**Teorema**:
		Suponha que $x_0, x_1,x_2,..x-n$ sejam todos distintos. Então, existe um único polinômio $P_n(x)$ de grau $\leq n$ tal que $P(x_i)=y_i$, i=0,1,2,3,...n

	- ### Em outra base:
		- $P(x) = a_0l_0(x) + a_1l_1(x) + ... + a_nl_n(x)$ ; Onde ${l_0,l_1,...l_n}$ é uma base para o espaço dos polinômios de grau menor ou igual a n.
		
		
		Matricialmente
		$$\begin{bmatrix}
		l_0(x_0) &l_1(x_0)& ... & l_n(x_0)\\
		l_0(x_1) & l_1(x_1)&... & l_n(x_1)\\
		...& ...&... &...\\
		l_0(x_n) &l_1(x_n)& ... & l_n(x_n)
\end{bmatrix} . \begin{bmatrix} a_0\\
a_1\\
...\\
a_n\end{bmatrix} = \begin{bmatrix} y_0\\
y_1\\
...\\
y_n\end{bmatrix}$$
			- O sistema ficaria simples
				- Identidade
				- Diagonal
				- Triangular
			--> Fazendo a identidade
			
		Em A, $a_{ij} = l_{j-1}(x_{(i-1)})$; para que A = I
		$l_0(x_i) = \begin{cases} 1; i=j\\ 0;i\neq j \end{cases}$ ; para J fixo, $l_j(x_i) =0$, $i \neq 1$ (n condições)
		$$\begin{bmatrix}
		l_0(x_0) &l_1(x_0)& ... & l_n(x_0)\\
		l_0(x_1) & l_1(x_1)&... & l_n(x_1)\\
		...& ...&... &...\\
		l_0(x_n) &l_1(x_n)& ... & l_n(x_n)
\end{bmatrix} = \begin{bmatrix} 1 &0&...&0\\ 0 & 1 & ... &0\\...&...&...&...\\ 0&0&...&1\end{bmatrix}$$
		
		Logo:
		$\displaystyle l_j(x) = \frac{(x-x_0)(x-x_1)...(x-x_{j-1})(x-x_{j+1})...(x-x_n)}{(x_j-x_0)(x_j-x_1)...(x_j-x_{j-1})(x_j-x_{j+1})...(x_j-x_n)}$
		
		##### Exemplo:
		
| x   | y   |
| --- | --- |
| 1   | 1   |
| 2   | 7   |
| 3   | 13  |
	
	$$\displaystyle \large \begin{cases}
    l_0 = \frac{(x-x_1)(x-x_2)}{(x_0-x_1)(x_0-x_1)} = \frac{(x-2)(x-3)}{(1-2)(1-3)}\\
    l_1 = \frac{(x-x_0)(x-x_2)}{(x_1-x_0)(x_1-x_2)} = \frac{(x-1)(x-3)}{(2-1)(2-3)}\\
    l_2 = \frac{(x-x_0)(x-x_1)}{(x_2-x_0)(x_2-x_1)} = \frac{(x-1)(x-2)}{(3-1)(3-2)}
    \end{cases}$$
    O polinômio tem forma $P(x) = 1l_0(x)+7l_1(x)+13l_2(x)$
    
```functionplot
---
title: Gráfico da curva obtida do ajuste
disableZoom: false
bounds: [0, 4, 0, 17]
grid: true
xLabel: x
yLabel: y
---

f(x) = (x-2)*(x-3)/2 + 7*(x-1)*(x-3)/(-1) + 13*(x-1)*(x-2)/2 

```


### ==Analise do erro==
- Seja f:[a,b] -> Reais e consiste {$(x_0,y_0),...(x_n,y_n)$} com $a \leq x_0 \leq x_1 \leq ... \leq x_n \leq b$

  Supomos que:
	  **f** tem pelo menos (n+1)[[Derivada]]s contínuas
	  **P** é o polinômio interpolador para **f** em $\displaystyle x_0, x_1, ...x_n$ 
	  **P** tem no máximo grau n
	  Definimos
	  $E(x) := f(x) -p(x)$ ; Seja x fixo , $x \neq x_k$ ; k=0 ,1 ,2 ,...n

- Consideramos também a função auxiliar
	$g(z) := E(x)\omega(z) - E(z)\omega(x)$; onde $\omega(z) := (z-x_0)(z-x_1)...(z-x_n)$ 
--> Como g tem pelo menos n+2 zeros, e é diferenciável, pelo [[Teorema do valor médio]]. g' tem pelo menos (n+1) zeros. Analogamente, g'' tem pelo menos n zeros -> $g^{(n+1)}$ tem pelo menos 1 zero

| **Função** | **Quant. zeros** |
| ---------- | ---------------- |
| $g$          | (n+2)            |
| $g'$        | (n+1)            |
| $g''$        | (n)              |
| $g^{(3)}$       | (n-1)            |
| $g^{(4)}$  | (n-2)            |
| .          | .                |
| .          | .                |
| .          | .                |
| $g^{(n)}$   | 2                |
| $g^{(n+1)}$ | 1                |
| $g^{(n+2)}$ | 0                 |

- Seja $\psi$ um zero de $g^{(n+1)}$ --> $\displaystyle g^{(n+1)(\psi)} =0$ -->$\omega (z) = z^{n+1}+ q(z)$; sendo q um polinômio de grau n

Por fim, temos ---> $\displaystyle E(x)= \frac{f^{(n+1)}}{(n+1)!}(\omega) \leq \frac{máx(f^{(n)})}{n!} máx|\omega(x)|$   
Exemplos:
	Caso de f(x)= $\sqrt{x}$ ,$x_0 =1$, $x_1=2$ e $x_2=4$; Qual o erro máximo? 
	$máx|\omega(x)|$ = $máx|(x-1)(x-2)(x-4)|$ --> $\displaystyle \frac{d(x^3-7x^2-2x-8)}{dx}$= 0 --> $3x-14x-2=0$ --> $\frac{+14\pm \sqrt{14^2-4.3.(-2)}}{2.3}$= 4,8053	
	$\displaystyle \frac{máx(f^{(n)})}{n!}$ ; f'(x) = $\displaystyle \frac{1}{2\sqrt{x}}$ ; f''(x)= $\displaystyle -\frac{1}{4\sqrt[2]{x^3}}$ ; f'''(x) = $\displaystyle \frac{3}{8\sqrt[2]{x^5}}$; o máximo é x=1 --> $\displaystyle \frac{3}{8}$ 	
	Assim:
	$\displaystyle \frac{máx(f^{(n)})}{n!} máx|\omega(x)|$ = $\frac{3/8}{3!}.4,8053$ = 0,30 --> Este é o erro máximo que pode ocorrer nesta aproximação
	.
	.
	Outro exemplo: Com que precisão podemos aproximar $\sqrt{115}$ usando interpolação quadrática sobre os pontos 100,121 e 144?
	
| x   | $\sqrt{x}$ |
	| --- | ---------- |
	| 100 | 10         |
	| 121 | 11         |
	| 144 | 12         |

Aproximação quadrática tem 3 pontos --> $\omega(x)=(x-100)(x-121)(x-144)$
máx(|$\displaystyle \omega(x)$|) = |$\omega '(x)$| = |$43924 - 730 x + 3 x^2$|=0--> x= 134
$\displaystyle \frac{máx(f^{(n)})}{n!}$ = $\displaystyle \frac{3}{8}$ 


### Algoritmos:
- ### Pseudo-algoritmo
  
	x <- Vetor com pontos da malha 
	n <-- length(x)
	L <- vetor de tamanho length(x) para armazenar a  base identidade
	Produto <-- $(x-x_0)(x-x_1)(x-x_2)...(x-x_{n-1})$
	- ##### Para i de 0 até n-1:
		L(i) <--  1/($x-x_i$)
		- ##### Para k de 0 até n-1
			- Se k for diferente de i:
				L(i)<-- L(i)/($X_i-x_k$)


- ### Algoritmo em Octave
	```octave
	  function yr = lagrange(x_c, x, y)
	%{ 
	A função encontra uma aproximação pontual por lagrange dado uma malha x e y discreta
     x_c: é o ponto x que queremos a aproximação
     y: vetor dado
     x: vetor x para construir o polinômio
	
	%}
	  yr = 0;
	  n = length(x);
	  for i=1:n
        p = 1;
        for j=1:n
            if j != i   % avoiding fancy division by 0
             p *= (x_c-x(j)) / (x(i)-x(j));
            endif;
        endfor;
        yr += y(i) * p;
	    endfor;
        endfunction;


	function [X,Y] = ilagrange(x,y,N);
	  %{ 
		 Dado uma malha x,y encontramos uma aproximação por interpolação com n pontos
	     x: vetor dado 
	     y: vetor dado
	     N: Número inteiro positivo
	  %}
		
	  X = linspace(x(1),x(end),N); # cria os pontos que queremos a aproximação
	  Y = ones(1,N); # cria o vetor que armazenará a identidade;
	
	  for i = 1:length(X)
	    Y(i) = lagrange(X(i), x,y);
	  endfor
	     
	endfunction
	
	x = [1 2 3 4 5];
	y = [3 2 1 2 2];
	[X,Y] = ilagrange(x,y,11)

	```

Usando função interna do octave
```octave
function [X,Y] = imatoct(x,y,N);
%{
	Dado valores um vetor x e y, e N sendo a quantidade de pontos desejamos de aproximação entre os valores inicial e final de x; Calcula uma aproximação por interpolação neles
	x: vetor que pegaremos os pontos para calcular
	y: Valor que sabemos em pontos discretos de x
	N: Quantidade de pontos que queremos entre o valor inicial e final de x
%}

X = linspace(x(1),x(end),N); # cria os pontos que queremos a aproximação
Y = ones(1,N); # cria o vetor que armazenará a identidade;
p1 = polyfit(x,y,length(x)-1); # Encontra o polinômio interpolador
	
for i =1:N # Calcula o valor para cada ponto de X
Y(i) = polyval(p1, X(i)); # cálcula o polinômio para cada valor dado de X
endfor
endfunction

x = [1 2 3 4 5];
y = [3 2 1 2 2];
[X,Y] = imatoct(x,y,11)
```

- Quando escolhemos sucessivos polinômios de ordem grande, e sendo os pontos equidistantes: o erro tende a aumentar


- ## ==Interpolação polinomia por partes== - Spline
	- ### por retas
		Separamos os pontos em pequenos grupos
		$Erro_{max}=max(E_j(k))$; que é o erro máximo de algum dos intervalos
			$máx|E_j| \leq \frac{máx|f''(z)|}{2}máx|(x-x_{j-1})(x-x_{j})|$ --> $\displaystyle E_{max} \leq \frac{M_2h^2}{8}$ 

		Exemplo: **Em quantos pontos regulares em [0,2] e com função f(x)=(2x+1)/(x-3) tenha um erro menor que  10^-4, com spline linear?**
			$f''= \frac{14}{(x-3)^3}=0$--> máx é x=2 --> $M_2 = 14$
			$M_2 \frac{h^2}{8} \leq 10^{-4}$ --> $h \leq \sqrt{8.10^{-4}}$ ; h=tamanho de intervalo/n pontos amostrais
			--> n > 265
	- ### Por parábolas

```octave
function yr = lagrange(x_c, x, y)
	%{ 
	A função encontra uma aproximação pontual por lagrange dado uma malha x e y discreta
     x_c: é o ponto x que queremos a aproximação
     y: vetor dado
     x: vetor x para construir o polinômio
	
	  %}
	  yr = 0;
	  n = length(x);
	  for i=1:n
        p = 1;
        for j=1:n
            if j != i   % avoiding fancy division by 0
             p *= (x_c-x(j)) / (x(i)-x(j));
            endif;
        endfor;
        yr += y(i) * p;
	    endfor;
        endfunction;

function [X,Y] = ilagrange(x,y,N);
  %{ 
     x: vetor dado 
     y: vetor dado
     N: Número inteiro positivo
  %}
	
  X = linspace(x(1),x(end),N); # cria os pontos que queremos a aproximação
  Y = ones(1,N); # cria o vetor que armazenará a identidade;

  for i = 1:length(X)
    Y(i) = lagrange(X(i), x,y);
  endfor
  return
     
endfunction

function [X,Y] = imatoct(x,y,N);
%{
	Dado valores um vetor x e y, e N sendo a quantidade de pontos desejamos de aproximação entre os valores inicial e final de x; Calcula uma aproximação por interpolação neles
	x: vetor que pegaremos os pontos para calcular
	y: Valor que sabemos em pontos discretos de x
	N: Quantidade de pontos que queremos entre o valor inicial e final de x
%}

X = linspace(x(1),x(end),N); # cria os pontos que queremos a aproximação
Y = ones(1,N); # cria o vetor que armazenará a identidade;
	p1 = polyfit(x,y,length(x)-1); # Encontra o polinômio interpolador
	
	for i =1:N # Calcula o valor para cada ponto de X
	Y(i) = polyval(p1, X(i)); # cálcula o polinômio para cada valor dado de X
	endfor
endfunction

# POntos equidistantes

dif_l = zeros(1,50); # vetor que armazenará o erro de ilagrange
dif_m = zeros(1,50);# vetor que armazenará o erro de imatoct
f = @(x) (1+x.^2).^-1; # a função que queremos aproximar

for n=1:50

x = linspace(-5,5,n); # cria pontos igualmente espaçados
y = f(x);

[Xl,Yl] = ilagrange(x,y,201); # chamamos a função ilagrange
[Xm,Ym] = imatoct(x,y,201); # chamamos a função imatoct
y = f(Xl); # calculamos o valor exato na mesma malha

# obtemos o maior erro
#dif_l(n) = max(y-Yl); 
dif_l(n) = norm(y-Yl, inf);
#dif_m(n) = max(y-Ym);
dif_m(n) = norm(y-Ym, inf);
endfor

# Plotamos os gráficos da norma pelo n, em semilog

semilogy(1:50, dif_l, 'r'); # plota o gráfico monolog do erro máximo para cada n
title('Erro da função ilagrange em função do grau do polinômio');
xlabel('Grau do polinômio');
ylabel('Logaritmo da norma do vetor erro');
ref
semilogy(1:50, dif_m,'b'); # plota o gráfico monolog do erro máximo para cada n
xlabel('Grau do polinômio');
ylabel('Logaritmo da norma do vetor erro');
title('Erro da função imatoct em função do grau do polinômio');
dweqd

# POntos não eequidistantes




dif_l = zeros(1,50); # vetor que armazenará o erro de ilagrange
dif_m = zeros(1,50);# vetor que armazenará o erro de imatoct
for n=1:50
f = @(x) (1+x.^2).^-1; # a função que queremos aproximar
x = -5*cos(pi*[1:n]/n); # equação para pontos de 1 até n
y = f(x);

[Xl,Yl] = ilagrange(x,y,201); # chamamos a função ilagrange
[Xm,Ym] = imatoct(x,y,201); # chamamos a função imatoct
y = f(Xl); # calculamos o valor exato na mesma malha

# obtemos o maior erro
dif_l(n) = norm(y-Yl, inf); 
dif_m(n) = norm(y-Ym,inf);
endfor

# Plotamos os gráficos da norma pelo n, em semilog

semilogy(1:50, dif_l, 'r');
title('Erro da função ilagrange em função do grau do polinômio');
xlabel('Grau do polinômio');
ylabel('Logaritmo da norma do vetor erro');

semilogy(1:50, dif_m,'b');
xlabel('Grau do polinômio');
ylabel('Logaritmo da norma do vetor erro');
title('Erro da função imatoct em função do grau do polinômio');


# Analisamos para n= 49
n=49
f = @(x) (1+x.^2).^-1; # a função que queremos aproximar
x = -5*cos(pi*[1:n]/n); # equação para pontos de 1 até n
y = f(x);

[Xl,Yl] = ilagrange(x,y,201); # chamamos a função ilagrange
[Xm,Ym] = imatoct(x,y,201); # chamamos a função imatoct
y = f(Xl); # calculamos o valor exato na mesma malha

#Plotamos a aproximação e a função 
hold on;
scatter(Xl,Yl, 'r');
fplot(f,[-5,5]);
title('Resultado da interpolação com n=49 para a função ilagrange e a função');
xlabel('Eixo x');
ylabel('Eixo y');
hold off;

hold on;
scatter(Xl,Yl, 'r');
fplot(f,[-5,5]);
title('Resultado da interpolação com n=49 para a função imatoct e a função');
xlabel('Eixo x');
ylabel('Eixo y');
hold off;




```