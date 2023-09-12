- Tem a ideia do [[Método de Newton]] de aproximação linear

Newton para sistemas não lineares

$\begin{cases} f_1(x_1,x_2,x_3,...x_n)=0\\f_2(x_1,x_2,x_3,...x_n)=0\\ f_3(x_1,x_2,x_3,...x_n)=0 \\ f_n(x_1,x_2,x_3,...x_n)=0\end{cases}$ ; Supondo que a equação é diferenciável 

_Exemplo_
$\large \displaystyle \begin{cases} x_1^2 +x_2^2-2=0\\ x_1^2- \frac{x_2^2}{9}-1=0\end{cases}$
```functionplot
---
title: Função dada pelas equações acima
disableZoom: false
bounds: [-2, 2, -2, 2]
grid: true
xLabel: x
yLabel: y
---

f(x,y) = (2-x^2)^(1/2)
f(x) = -(2-x^2)^(1/2)
f(x) = 1+ (x^2)/9
f(x) = -1- (x^2)/9
```

Vamos fazer cada $f_i (x_1,x_2,...x_n)$ sua aproximação linear perto de $x^k$
$$f_i (\vec x) = f_i(\vec x^k)+ \frac{\partial f(x_1-x_1^k)}{\partial x_1} +...+ \frac{\partial f(x_n-x_n^k)}{\partial x_n}+ o(x-x^k) \approx f(\vec x^k)+\nabla f(\vec x^k)(x-x^k)$$
- Aproximamos com o [[Gradiente]]
Perto de $\vec x^k$, $f_i(\vec x)  \approx l_i(\vec x)$
Vamos trocar o cálculo do zero verdadeiro de $f_i(x)$ pelo cálculo do zero de $L_i(x)$ e vamos chamar o resultado de $\vec x^{k+1}$
$$\begin{cases} 0 = f_1(\vec x^k)+ \frac{\partial f(x_1-x_1^k)}{\partial x_1} +...+ \frac{\partial f(x_n-x_n^k)}{\partial x_n} \\
0 = f_2(\vec x^k)+ \frac{\partial f(x_1-x_1^k)}{\partial x_1} +...+ \frac{\partial f(x_n-x_n^k)}{\partial x_n} \\
...\\ 
0 = f_i(\vec x^k)+ \frac{\partial f(x_1-x_1^k)}{\partial x_1} +...+ \frac{\partial f(x_n-x_n^k)}{\partial x_n}\end{cases}$$
que pode ser escrito como
$$\begin{bmatrix} \frac{\partial f_1}{\partial x_1}&...& \frac{\partial f_1}{\partial x_n} \\ ... \\ \frac{\partial f_n}{\partial x_1}&...& \frac{\partial f_n}{\partial x_n}\end{bmatrix} \begin{bmatrix} x_1^{k+1}-x_1-^k\\...\\ x_n^{k+1}-x_n^{k}\end{bmatrix}= \begin{bmatrix} f_1(\vec x^k)\\...\\f_n(\vec x^k) \end{bmatrix}$$
Assim o sistema linearizado fica em função da [[Jacobiana]]
$J(x^k)\underbrace{(x^{k+1}-x^k)}_{\vec d}=-f(x^k)$ 

$J.\vec d = - \vec f (\vec x^k)$ e assim a cada passo temos um [[Sistema linear]] para ser resolvido e encontrar $\vec d$ 
$$\begin{cases} J(\vec x^k)\vec d^k = -\vec f (\vec x^k)\\ \vec x^{k+1} = \vec x^k+\vec d^k\end{cases}$$
- pseudo-algoritmo
	x <-- $\vec x^0$ 
	k = 0
	j = J(x) # avaliamos a [[Jacobiana]]
	f = f(x) # avaliamos a função
	Resolver o sistema $\begin{cases} J(\vec x^k)\vec d^k = -\vec f (\vec x^k)\\ \vec x^{k+1} = \vec x^k+\vec d^k\end{cases}$
	

	```octave
	function x = sistema_ninear(x0, jacobiana, func)
		j = jacobiana(x0) # jacobiana
		f = func(x0); # função
		x = j\(f*(-1)) # aproximação primeira iteração
		x=x'
		cont=0;
		
		while norm(x-x0, inf) > 10^-15 && cont < 200
			j = jacobiana(x);
			f = func(x);
			t = j\(f*(-1));
			x = x + t';
			cont+=1;
		endwhile
	endfunction
	```