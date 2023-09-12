Para denotar a operação, usamos o símbolo $\large \mathscr{L}(f(t))$  e foi mulito usada por [[Pierre lamon Laplace]]. E é definida como uma [[Integral imprópria]] e está na classe maior de [[Transformada integral]]. [[Integral]]

$\displaystyle \large\mathscr{L} (f(t)) = \int_{0}^{\infty} e^{-St}f(t)dt = \lim_{B \to \infty} \int_{0}^{B} e^{-St}f(t)dt$

- **Vantagens**
	1. A transformada leva a [[EDO]] em uma equação algébrica
	2. Não é necessário calcular $y_c$ e $y_p$ 

- $\textbf{Teorema}$
1. f é seccionalmente contínua no intervalo $0 \leq t \leq A$ para qualquer A positivo
2. Existem constantes reais $k$ , a e M, com K e M positivas, tais que 
 $|f(t)| \leq Ke^{at}$ Quando $t \geq M$ 
 Então, a transformada de Laplace, definida pela Eq.(4) existe para s>a
- **Tabela de Laplacianas**

| Função| Laplaciana | Nº   | Restrição             |
| ------------------------------------------------------ | --------------------------------------------------- | ---- | --------------------- |
| a (constante)| $\large a\frac{1}{S}$      | (1)  | S>0     |
| $e^{at}$                                               | $\large \frac{1}{S-a}$                              | (2)  | S-a>0 e S>a           |
| $Cosh(kt)$                                             | $\large \frac{S}{S^2-K^2}$                          | (3)  | S> $\text{pip k pip}$ |
| $Senh(kt)$                                             | $\large \frac{K}{S^2-k^2}$                          | (4)  | S > pipe k pipe       |
| $Cos (kt)$                                             | $\large \frac{S}{S^2+K^2}$                          | (5)  | S>0                   |
| $Sen (kt)$                                             | $\large \frac{K}{S^2 +K^2}$                         | (6)  | S>0                   |
| $t^a$                                                  | $\displaystyle \large \frac{\Gamma (a+1)}{S^{a+1}}$ | (7)  | S>0                   |
| $u_a(t)$                                               | $\displaystyle \large \frac{e^{-aS}}{S}$            | (8)  | S>0                   |
| $e^{at}sen(bt)$                                        | $\displaystyle \frac{b}{(s-a)^2+b^2}$               | (9)  | S>a                   |
| $e^{at}cos(bt)$                                        | $\displaystyle \frac{s-a}{(s-a)^2+b^2}$             | (10) | S>a                   |
| $\mathscr{L}\{\delta_a(t)\}$                           | $e^{-as}$                                           | (11) |                       |
| $\mathscr{L}\{u_c(t)\}$                                | $\displaystyle \frac{e^{-cs}}{s}$                   | (12) | s>0                   |
| $\mathscr{L}\{u_cf(t-c)\}$                             | $e^{-cs}\mathscr{L}\{f(t)\}$                        | (13) | s>a                   |
| $\displaystyle f(t) =\int_0^t g(t)dt$; $\mathscr{L}\{f(t )\}$ | $\frac{1}{S} \mathscr{L}\{f(t)\}$                  | (14)     |                       |


**Prova da Nº1:**
	$\displaystyle \large \int_{0}^{\infty} ae^{-St}dt = a\lim_{B \to \infty} \left[ \frac{e^{-St}}{-S}|_{0}^{b} \right] = a \lim_{B \to \infty} \left[ \frac{e^{-Sb}}{-S}- \frac{1}{-S}\right]$, e temos a restrição de que S > 0 para haver convergência   

**Prova da Nº2:**
$\displaystyle \large \int_{0}^{\infty} e^{at}e^{-St}dt = \int_{0}^{\infty} e^{-(S-a)t}dt$

Aplicamos a transformada em uma [[EDO]] na forma $ax'' + bx' +cx= f(x)$  
$\mathscr{L}(ax'' + bx' +cx= f(x))$, como a transformada é linear  
$a\mathscr{L}(x''(t))+ b\mathscr{L}(x'(t))+c\mathscr{L}(x(t))= \mathscr{L}(f(t))$  
**Prova da Nº 7:**
$\displaystyle \large \mathscr{L} (t^a) = \int_0^\infty e^{-st}t^adt$, Aplicamos o [[Método da substituição]] $\begin{cases}u=st\\ du =sdt \end{cases}$ , com os mesmos limites de integração
$\displaystyle \int_{0}^\infty e^{-u}\left(\frac{u}{S}\right)^a\frac{du}{S}=\frac{1}{S^{a+1}} \int_0^\infty e^{-u}u^a du$ e está integral é a [[Função Gamma]]. Então:
$\displaystyle \mathscr{L}(t^a) = \frac{\Gamma (a+1)}{S^{a+1}}$

**Prova da Nº8**
temos a [[Função degrau]]
$\displaystyle \mathscr{L}(u_a(t)) = \int_{0}^\infty e^{-St}u_a (t)dt= \int_{0}^a e^{-St}.0 + \int_{a}^\infty e^{-St}.1dt = \frac{e^{-St}}{-S}|_{a}^\infty = \frac{e^{-aS}}{S}$
- **Definição**  
Se f é derivável por partes, então f também é contínua por partes e diferenciável em [a,b] a menos de um nº finito de pontos e f' também é contínua por partes  
  
$\textbf{Teorema}$ - [[Teorema da transformada da derivada]]  
Seja $f$ [[Contínua]] e diferenciável por parte, f tem ordem exponencial; então  
$$\mathscr{L}(f'(t))= s\mathscr{L}(f(t))-f(t)$$  
**Demonstração:** Suponha que f' é contínua  
	$\mathscr{L}(f'(t))= \int_{0}^{\infty} e^{-st}f'(t)dt$, resolvendo por partes $\begin{cases}u = e^{-st}\\ dv = f'(t)dt \\du = -se^{-st}dt \\ v= f(t)\end{cases}$  
	  $\displaystyle \large \lim_{b \to \infty} e^{-st}f(t)|_{0}^b - \int_{0}^\infty -se^{-st}f(t)dt$ ;  $\displaystyle \lim _{b \to \infty} e^{-sb}f(b)-f(0) + s \int_{0}^{\infty}e^{-st}f(t)$  
	  este limite nos retorna o [[limite]] da exponencial é 0 e o termo com a [[Integral]] é a definição da laplaciana  
	_obs_: para f contínua por partes  
	$\displaystyle \mathscr{L} (f'(t))= s\mathscr{L}(f(t))-f(0)- \sum_{i=1}^{\infty}e^{-st}j(t_i)$  
	**Corolário**:  
	$\mathscr{L}(f''(t))$,    f'(t)=g(t) $\Rightarrow \mathscr{L}(g'(t))= s \mathscr{L}(g(t))-g(0)= s\mathscr{L}(f'(t))-f'(0)=s[s\mathscr{L}(f(t))-f(0)]-f'(0)= s^2 \mathscr{L} -sf(0)- f'(0)$  
_**Exemplo**_  
$x''(t) -x'(t)-6x(t)=0$  
Usando corolário de laplace  
$[s^2 X(s)-sx(0)-x'(0)]-[s\mathscr{x(t)}-x(0)]-6X(s)=0$  
$\displaystyle X(s)[s^2-s-6]= -2-1+2s \Rightarrow X(s)= \frac{2s-3}{s^2-s-6}$ , as raízes são $(1 \pm 5)/2$  
$\displaystyle \frac{2s-3}{(s-3)(s+2)}= \frac{A}{s-3}+ \frac{B}{s+2}$, A= 3/5, B=7/5, Usamos a tabela de inversas  
$\displaystyle \mathscr{L}^{-1}(\frac{3/5}{s-3})= \frac{3}{5}e^{3t}$  
$\displaystyle \mathscr{L}^{-1}(\frac{7/5}{s-6})= \frac{7}{5}e^{-2t}$


$\textbf{Teorema}$: [[Teorema de existência da transformada de Laplace]]
	Supomos que a função seja contínua por partes e f(t) possui [[Ordem exponencial]]. isto é, existem constantes M,c,T, são não negativas de modo que$$|f(t)| \leq M e^{ct},\text{Para }~~~~ t \geq T$$
	E estas são condições suficientes para que a transformada de f(t) para s>c
	_Exemplo_
	$\displaystyle \mathscr{L}(8t^3)+5t+cos(8t) = 8 \frac{3!}{s^{4}}+5\frac{\Gamma (7/2)}{S^{7/2}}+\frac{S}{S^2+64}$ 

**Teorema da transformada da integral**
	Seja f(t) = $\displaystyle \int_0^t g(t)dt$ contínua por partes e com ordem exponencial 
	Calculamos $\mathscr{L}\{f'(t)\}$ que é $s\mathscr{L}\{f\} - f(0)$, f(0) = 0
	isolamos a transformada de f e temos 
	$$\mathscr{L}\{f(\tau )d\tau\}=\frac{1}{S} \mathscr{L}\{f(\tau)\}$$

[[Produto convolução]]

def f,g continua por partes com ordem esponecial t -> $\infty$ 

$\displaystyle \large f~.~g = \int_{0}^t f(\tau)g(t-\tau)d\tau$ 
$\large \mathscr{L}\{f\cdot g\}= F(S)G(S)$ <=> $\mathscr{L^{-1}}\{F(S)G(S)\} = f(t)\cdot g(t)$

_Exemplo_:
$\displaystyle \mathscr{L^{-1}} \{\frac{S}{S^2+1}. \frac{1}{S^2+1}\}= cos(t)\cdot sen(t) = \int_{0}^t cos(\tau) sen(t-\tau)d\tau$ = $\displaystyle \int_{0}^t cos (\tau) [sen (t) cos(-\tau)+cos(t)sen(-\tau)]d\tau= sen(t)\int_0^tcos^{2}(\tau)-cos(t)\int_0^t sen(\tau)cos(\tau)$ 
= $\displaystyle \frac{1}{2}t \sin (t)$ 

$\textbf{Teorema}$ [[Derivada de uma transformada de Laplace]]
$$\mathscr{L}[t f(t)]= -\frac{d}{ds}\mathscr{L}\{f(t)\}$$