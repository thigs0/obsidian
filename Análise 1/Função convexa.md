Uma função é convexa se
$$f(x)\leq f(a)+\frac{f(b)-f(a)}{b-a}(x-a)~~ou~~f(x)\leq f(b)+\frac{f(b)-f(a)}{b-a}(x-b)$$

#### Teorema
Se f é uma [[Função convexa]] no intervalo. Então existe $f_+'(c)$,$f_-'(c)\forall c\in int(I)$
$c\in int(I)$ 
$$\varphi_c(x)=\frac{f(x)-f(c)}{x-c}\forall x\in J=I\cap (c,\infty)$$
**Demonstração**
$\varphi_c(x)=$ não é crescente. $\displaystyle \varphi_c(x)\frac{f(x)-f(c)}{x-c}\leq \frac{f(y)-f(c)}{y-c}=\varphi_c(y);~~x\leq y$ 
Vamos provar que $\varphi_c(x)$ é limitada inferiormente, como $c\in int(I),~\exists a\in I;a<c<x$ 
$$\varphi_c(x)=\frac{f(x)-f(c)}{x-c}\geq \frac{f(c)-f(a)}{c-a}$$

1) $f$ é convexa
2) A [[Derivada]] $f'$ é uma [[função monôtona]] não descrescente
3) $\forall a,x\in I$, $f(x)\leq f(a)+(x-a)f'(a)$

**Demonstração**
1 --> 2
$a<x<b$
$$\frac{f(x)-f(a)}{x-a}\leq \frac{f(b)-f(a)}{b-a}\leq \frac{f(x)-f(b)}{x-b}$$
$$f'(a)=f_+(a)\leq f_-(b)=f'(b)$$
2-->3
Tomo a< x; $(a,x)\exists c\in (a,x)$
$f(x)-f(a)=f'(c)(x-a)\Rightarrow \begin{align}f(x)=f'(c)(x-a)+f(a) \\ \geq f'(a)(x-a)+f(a)\end{align}$

3-->1
Provar e entregar
##### Corolário
Todo [[Ponto extremo]] de uma função convexa é um ponto mínimo
$$f(x)\geq f(a)+(x-a)f'(a)$$
Seja a um [[Ponto extremo]], $f'(a)=0$, $f(x)\geq f(a)\forall x\in I$

##### Corolário
$f:I\to \mathbb{R};\exists f''$ f é convexa <--> $f''(x)\geq 0$
f é convexa <--> $f'(x)$ é monotona não decrescente <--> $(f'(x))'\geq 0$

**Definição**
$f:I\to \mathbb{R}$ é uma [[Função Concava]] se $-f$ é uma [[Função convexa]]  