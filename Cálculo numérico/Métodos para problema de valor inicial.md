Criamos Métodos para tentar resolver uma [[EDO]] de forma valor inicial
- EDO de n ordem, tem n incógnitas
- Dirichet --> Se tem o valor da função e encontra a constante


 - #### Problema padrão
	 $y'(t) =f(t,t(t))$ ;    $t>t_0$
	 $y(y_0)=y_0$

	- $\textbf{Teorema}$ -> Supomos que:
		1. f é contínua em R
		2. f é [[Lipschitz]] contínua em y
		3. Caso a edo seja de ordem superior, usamos o [[Método de redução de ordem]]

- ### Método de Euler
	- $\displaystyle y_1 \approx t_1 =y_{(t_0+h)}$ 
	
	Usamos o [[Polinômio de Taylor]] e obtemos:
	
	$y(t_0)+hy'(t_0)+\frac{h^2}{2}y''(\xi)$  

	- ###### Aproximação
		$y_1 = y_0 +hf'(t_0,y_0)$ 
		$y_{n+1}=y_n +hf(t_n),y_n$ 

	- _Exemplo_
		1)
		
			 $$\begin{cases}x'(t) = \sigma(y-x)\\
			 y'(t) = x(\rho -z)-y\\
			 z'(t) = xy-\beta z
			 \end{cases}$$
			 Em que $\sigma=10 ,\rho=28, \beta=8/3$
			 Denotamos o vetor Y como     -->       $Y(x,y,z,t) = (\sigma(y-x), x(\rho -z)-y, xy-\beta z)$
				
		```octave
			sigma = 10;
			rho = 28;
			beta = 8/3;
			
			f_ = @(x, y, z, t) [sigma*(y - x); x*(rho - z) - y; x*y - beta*z];
			
			f = @(v, t) f_(v(1), v(2), v(3), t);
			
			function retval = euler(f, t, v0, h)
			  N = length(t);
			  retval = zeros(3, N);
			
			  retval(:, 1) = v0;
			
			  for i = 1:N-1
			    retval(:, i+1) = retval(:, i) + h.*f(retval(:, i), t(i));
			  endfor
			
			endfunction
			
			t = 0:1e-2:100;
			
			v0 = [-6; -6; 15];
			
			Ve = euler(f, t, v0, 1e-2);
			
			Vo = lsode(f, v0, t);
			
			plot3(Ve(1,:), Ve(2,:), Ve(3,:), 'b');
			grid on;
			
			print('/home/thiagosilva/Imagens/Euler.png')
			
			plot3(Vo(:,1), Vo(:,2), Vo(:,3), 'r');
			grid on;
			
			print('/home/thiagosilva/Imagens/lsode.png')
			
			plot3(Ve(1,:), Ve(2,:), Ve(3,:), 'b');
			grid on;
			hold on;
			plot3(Vo(:,1), Vo(:,2), Vo(:,3), 'r');
			print('/home/thiagosilva/Imagens/ambas.png')
			hold off;
			
			plot3(Ve(1,:) - Vo(:,1)', Ve(2,:) - Vo(:,2)', Ve(3,:) - Vo(:,3)', 'k');
			grid on;
			
			print('/home/thiagosilva/Imagens/diff.png')
			
			save res_Euler Ve
			save res_lsode Vo
			```
			 
		2. [[Equação do pêndulo]]
			$\begin{cases} \theta''(t) + k_1 \theta'(t) +k_2Sen(\theta(t))=0\\ \theta(0) = \frac{\pi}{3}\\ \theta'(0) = 0\end{cases}$; Fisicamente $k_1 = \frac{B}{mL^2}$ e $K_2 = \frac{g}{L}$
			
			Definindo f(t) = $\theta'(t)$ --> $\begin{cases} \theta'(t) = f(t)\\ f'(t) = k_1f(t) -k_2Sen\theta(t)\end{cases}$
			
			
			
- ## [[Runge-Kutta]]
	- Tão correto quanto taylor
	- Não precisa avaliar a derivada
	- Múltiplas avaliações de f
	Aproximamos a função y pela integral $\displaystyle \large y(t_{n+1})-y(t_n) = \int_{t_n}^{t_{n+1}} f(t,y(t))dt$
	- ### Método do trapézio ou [[Método de Heun]]
		Aproximamos a área da integral por um trapézio
		$$y_{n+1}=y_n + \frac{h_n}{2}[f(t_n,y_n)+f(t_{n+1},y_{n+1})]$$
		Reorganizando aproximamos $y_{n+1}$ da f com o método de euler, $f$ é a derivada e o sistema é:
		$$\begin{cases} \hat y = y_n + h_nf(t_n,y_n)\\y_{n+1}=y_n + \frac{h_n}{2}[f(t_n,y_n)+f(t_{n+1},\hat y)]\end{cases}$$
		##### Algoritmo
		- Octave
```octave
# Exemplo
y0 = 1;
yl = @(y,t) 1+(t-y)^2;
malha = y0:0.1:5

function Y = RungeKuttaT(y0,yl,malha)
h = malha(2)-malha(1) #Pegamos o intervalo
x= malha
Y = [y0] #Valores de aproximação
for i = 1:length(malha)-1 # ignoramos o ponto inicial e final
yhat = Y(i) + h*yl(Y(i),x(i));
Y(i+1) = Y(i) + (h/2)*[yl(Y(i),x(i)) + yl(yhat,x(i+1))];
endfor
endfunction

V = lsode(yl, y0, malha)
plot(malha,Y,'xr', malha,V,'xb')
```
```julia
function RungeKutta(y0, yl, malha)
    h = malha[2] - malha[1] #Passo
    x = malha
    Y = Vector{Float64}([y0]) # local de armazenamento
    for i in 1:length(malha)-1 # ignoramos o ponto final
	    yhat = Y[i] + h*yl(Y[i], x[i])
	    append!(Y, Y[i] + (h/2)*(yl(Y[i], x[i])+ yl(yhat, x[i+1])))
    end
    return Y
end
````

- ### Método do ponto médio
	Começamos novamente calculando a inclinação no início do intervalo que é a mesma que a do método de euler. A seguir calculamos um $u^e$ provisório dado por 
	$$u^e = u_n + \frac{\Delta t}{2}k_1, ~~~k_1 = f(t_n, u_n)$$
	ou seja esse é o u de euler no meio do intervalo. A seguir, calculamos a inclinação da solução neste ponto $u_e$, dado por
	$$k_2 = f(t_n+ \frac{\Delta t}{2}, u_n + \frac{\Delta t}{2}k_1)$$
	Usamos então esse $k_2$ para estimar $u_{n+1}$. Portanto, do ponto ($t_n,~u_n$)
$$u_{n+1} = u_n +k_2\Delta t$$
	Expandindo o lado direito da equação acima, pode-se mostrar que a ordem deste método é 2
```julia
function Ponto_Medio(fl, y0, malha)
	h = malha[2]-malha[1] #passo
    x = malha
    Y = Vector{Float64}([y0])

	for i in 1:length(x)-1
		#método de euler, pegamos o ponto médio
		e = Y[i]+ (h/2)*fl(Y[i], x[i]) 
       
		#Avaliamos a inclinação no ponto médio
		ue = fl(e + Y[i]*(h/2), x[i]+(h/2))

		#terminamos com euler inclinação do ponto médio
        append!(Y, Y[i]+ue*h)
        
	end

	return y
end
```

Estes dois métodos são exemplos do método de Runge-Kutta de 2º ordem que em sua forma geral é dada por 
$$u_{n+1} = u_n + \Delta t \beta_0 f(t_n, u_n) + \Delta t \beta_1 f(t_n+\gamma \delta t, u_n + \psi\delta t)$$
Os parâmetros $\beta_0, \beta_1, \gamma~ e~ \psi$ são escolhidos de maneira que o método seja de ordem 2. isto é começando fazendo a expansão em Taylor da expressão acima e exigimos que ele seja igual a do método de Taylor de ordem 2
Assim, temos
$$f(t_n, \gamma \Delta t , \psi \Delta t) = f(t_n, u_n) + \gamma \Delta t f_t (u_n, t_n)+ \gamma \Delta t f_u(t_n, u_n) + o(\Delta t^2)$$
substituindo, obtemos que 
$$\begin{cases} \beta_0 + \beta_1=1\\ 2 \beta_1 \gamma = 1\\ 2 \beta_1 \psi = f(t_n, u_n) \end{cases}$$
- ### Método de Taylor de ordem 2
	$\displaystyle y_{n+1}= y_n +hf(t_n,y_n)+\frac{h^2}{2!}[f_t(t_n,y_n)+f_y(t_n,y_n)f(t_n,y_n)]$ 

	- Mais custoso que Euler
	- Mais demorado que Euler
	- Mais preciso que Euler
	
	- ###### Erro de truncamento
		$\displaystyle y(t_n)-y_n = e_n \equiv \frac{h^{k+1}}{(k+1)!}y^{k+1}(\xi)$ ; N é o ponto da malha; K é a ordem de taylor
		
		$\displaystyle |e_n| \geq \frac{M_n}{(k+1)!}h^{k+1}$ ; $\displaystyle M_n = max_{\xi \in I} |y^{k+1}(\xi)|$
	**Exercício**
	Use o método de taylor calculado acima para achar uma aproximação para u(t)
	$\begin{cases} u' = -u+t+2 \\ \Delta t = 0\\ u(0) = 1; ~~ T=(0.3)\end{cases}$
		
### **Método de Euler implicito**
Aqui usamos a equação da diferença para trás para avaliar
$$\frac{du}{dt}|_{tn+1} = f(t_{n+1}, u(t_{n+1}))$$
Assim $\displaystyle \frac{du}{dt}|_{tn+1} \approx \frac{u_{n+1}-u_n}{\Delta t} \Rightarrow \frac{u_{n+1}-u_n}{\Delta t}$
$\displaystyle \large u_{n+1} = u_n + \Delta t f(t_{n+1}, u_{n+1})$

**Sistema de Equações**
Considere o sistema de m equações de primeira ordem
$\begin{cases} u'_1 = f_1(t_1, u_1,...u_1)\\ u'_2 = f_2(t_2, u_2,...u_2)\\..\\ u'_m = f_m(t_m, u_m,...u_m)\end{cases}$
que também pode ser escrito em notação vetorial $\frac{d\vec u}{dt} = \vec f (t, \vec u)$
com $\vec u = \begin{pmatrix} u_1\\ u_2\\ ...\\u_m\end{pmatrix}$; $\vec f = \begin{pmatrix} f_1 \\ f_2\\... f_m \end{pmatrix}$ O [[PVI]] associado corresponde a dar uma condição inicial $\vec u (0) = \vec u_1$ para $\vec u$ com isso, o método de Euler explícito fica 
$$\large \vec u_{n+1} = \vec u_n + \Delta t \vec f(t_n, u_n)$$