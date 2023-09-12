Dado um conjunto de dados esperimentais y em um eixo x e y são coluna


$\large \phi = c_1\phi_1 + c_2\phi_2 + ... + c_n\phi_n$ ; Definimos uma função que achamos que aproxime os pontos
para uma dada função y(x)
```functionplot
---
title: Função x^(x^-2)
disableZoom: false
bounds: [-2, 3, 0, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = x^(x^-2)
```
Está aproximação tem um erro, assim, a soma do [[Erro]] índividual é $\displaystyle ||\phi -y||^2 = \sum_{i=1}^n (\phi(x_i) - y_i)^2$ 

$$\phi = \begin{bmatrix}
c_1\phi_1(x_1) & c_2\phi_2(x_1)& ...& c_n\phi_n(x_1)\\
c_1\phi_1(x_2) & c_2\phi_2(x_2) & .. & c_n\phi_n(x_2)\\
... & ... & ...&...\\
c_1\phi_1(x_1) & c_2\phi_2(x_2) & ... & c_n\phi_n(x_n)
\end{bmatrix} = 
\phi c = \begin{bmatrix}
\phi_1(x_1) & \phi_2(x_1)& ...& \phi_n(x_1)\\
\phi_1(x_2) & \phi_2(x_2) & .. & \phi_n(x_2)\\
... & ... & ...&...\\
\phi_1(x_n) & \phi_2(x_n) & ... & \phi_n(x_n)
\end{bmatrix}.
\begin{bmatrix}
c_1\\
c_2\\
c_2\\
...\\
c_n
\end{bmatrix}$$
Para minimizarmos, usamos o 
$||\phi -y||^2 = (\phi -y)^2 = (\phi c-y)^T(\phi c - y) = c^T(\phi^T \phi)c -2c^T \phi^T y + y^Ty$ 

$min|\phi -y|^2 \Leftrightarrow \nabla(|\phi -y|^2) =0$
-> 

**Caso a função não seja linear**
	Usamos processos que preservem o sistema e o tornem linear
	*Exemplo*
	$\phi(X) = \alpha_1 e^{-\alpha_2 x} \xRightarrow {\text{ Aplicamos log}} \ln (\phi) = \ln (\alpha_1) - \alpha_2 x$
	
### Algoritmo
- Definição do espaço de aproximação
	Ex: Polinômios, exponenciais, trigonométricas
- Construa a matriz $\phi$
	A [[Geometria Analítica/Matriz]] tem a linhas sobre o mesmo ponto
- Calcule as [[Funções]]
	$\phi^T \phi$ é: simétrico e seja uma [[Matrix definida positiva]] -> $x^T Ax \geq 0$ e $x^T A x \geq 0$ <-> x=0
	$\phi^t y$
- Resolva o sistema 
	$\phi^t \phi ~x= \phi^ty$ 
- Compare o resíduo
	Calcular $||\phi-y||^2$ entre diferentes funções escolhidas e ver qual tem o menos
*Exemplo*
Suponha que queremos aproximar f(x) = $4x^3$ por uma reta no intervalo [0,1]
	Escolhemos $\phi_1(x)=1, \phi_2(x)=x$ => $\phi(x) = c_1 \phi_1(x)+c_2\phi_2(x)$
	$\phi = \begin{pmatrix} 1 & 4\\ 1 & 0 \end{pmatrix}$; $\phi^T = \begin{pmatrix} 1 & 4\\ 1 & 0 \end{pmatrix}$

| x   | 0    | 0.5 | 1    | 1.5  | 2   | 2.5 | 3   |
| --- | ---- | --- | ---- | ---- | --- | --- | --- |
| y   | 1.92 | 0.9 | 0.65 | 0.52 | 0.5 | 0.43 |  0.4   |


Podemos plotar os dados com o código
```octave
x = [0 ,0.5 ,1 ,1.5 ,2 , 2.5, 3];
y = [1.92, 0.9, 0.65, 0.52, 0.5, 0.43, 0.4];
plot(x, y,'or');grid on #plotamos os pontos em circulos vermelhos
```

Definimos uma equação $\phi(x) = \sqrt{1/(\alpha +\beta x)}$ , e temos que deixá-la na forma linear
$$\phi(x) = \sqrt{1/(\alpha +\beta x)} $$
$$\frac{1}{\phi(x)^2} = \alpha +\beta x = \Phi(x)$$
-Transformamos a equação original em uma equivalente em que temos os termos $\alpha$ e $\beta$ lineares
temos os novo pontos para linearizar
```octave
x= [0 ,0.5 ,1 ,1.5 ,2 , 2.5, 3];
y = [0.27127   1.23457   2.36686   3.69822   4.00000   5.40833   6.25000];
plot(x,y, 'or'); grid on
```

```octave
x= [0 ,0.5 ,1 ,1.5 ,2 , 2.5, 3]';
y = [0.27127   1.23457   2.36686   3.69822   4.00000   5.40833   6.25000]';

eq=@(x) [x.^0 , x]
function C = mmq(eq, x, y)
# termo da equação f(x) = æ+ßx
phi = ones(length(y),length(eq(1)))   # criamos uma matriz de um para calcular
for i=1:length(phi)
	phi(i,:) = eq(x(i));
endfor

A = phi'*phi
B = phi'*y
C = A\B
endfunction

eq=@(x) [x.^0 , x]
C = mmq(eq, x, y)
Y = @(x) sqrt(1./(C(1) + C(2) .*x))
plot(x,y,'ok',x',Y(x')); grid on

# termo da equação f(x) = æ.Sin(x) + ß.Cos(x) + µ.Cos(2.x)
x = [0 ,0.5 ,1 ,1.5 ,2 , 2.5, 3]';
y = [1.92, 0.9, 0.65, 0.52, 0.5, 0.43, 0.4]';

phi = ones(7,3)   # criamos uma matriz de um para calcular
phi(:,1) = sin(x)  
phi(:,2) = cos(x)
phi(:,3) = cos(2*x)

A = phi'*phi
B = phi'*y
C = A\B

Y = @(x) C(1)*sin(x) + C(2)*cos(x) + C(3)*cos(2*x)
plot(x,y,'ok',x,Y(x)); grid on
```

```functionplot
---
title: Gráfico da curva obtida do ajuste
disableZoom: false
bounds: [0, 3, 0, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = sqrt(1/(1.365357142857142 - 0.4035714285714284*x))
```

**Teste de alinhamento**
	Para se ter uma boa ideia sobre se o modelo linearizado é uma escolha válida podemos plotar os dados linearizados $(\bar x_{i}, \bar y_{i})$ em um diagrama de disperssão, como abaixo
	*Obs*: Sempre que linearizarmos o problema e então aplicamos o método dos quadrados mínimos lineares, estamos minimizando o erro do modelo linearizado e este em geral não corresponde a minimizar o erro do problema não linear original


**Caso usemos [[Processo de Gram-Schmidt]]**
	Transformamos a base $\{1,x,x^2,x^3,...\}$ no intervalo [-1,1] da reta, chegamos aos chamados [[Polinômio de Lagrange]]
	$\displaystyle \begin{cases} p_0(x) =1 \\ p_1(x)=x\\ p_2(x)=x^2- \frac{1}{3}\\ p_3(x) = x^3 - \frac{3}{5}x \\ ...\\...\end{cases}$ Qua são tais que $\displaystyle \int_{-1}^1 p_i(x)p_j(x)dx = \delta_{ij}$ 
	Podemos também alterar o [[Produto interno]] no espaço de funções adiconando uma função peso 
	e se a função peso com $\displaystyle W = \frac{1}{\sqrt{1-x^2}}$ obtemos os [[Polinômios de Chebyshev]]