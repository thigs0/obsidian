queremos um operador linear para o [[Produto interno]] generalizado $<u,v>=\int_a^b u(x)v(x)dx$ 

e queremos $<u(x),\mathbb{L}[v(x)]>=\int_a^b u(x)\mathbb{L}[v](x)dx$
$<\mathbb{L}^\dagger[u](x),v(x)>=\int_a^b \mathbb{L}^\dagger[u]v(x)dx$

- suponha $\mathbb{L}=P_2(x)\frac{d^2}{dx^2}+P_1(x)\frac{d}{dx}+P_0(x)$
que é um [[Subespaços]] das [[Funções]] contínuas e com [[Derivada]]s de modo
$$<u(x),\mathbb{L}[v]>=<\mathbb{L}^\dagger[u],v>$$ - impomos que $\int_a^b u\mathbb{L}(v)dx-\int_a^b \mathbb{L}^\dagger [u]vdx =\int_a^b \frac{d}{dx}\mathbb{Q}[u,v](x)dx$
resolvendo a primeira [[Integral]]
1. 
##### Exemplo
$y''+y=0$ => $\mathbb{L}=\left( \frac{d^2}{dx^2}+1 \right), \in C_0^\infty (-\pi,\pi)$ 


- é uma forma de olhar para uma [[EDO]]
- os coeficientes são reais
- são condições que não dependem da fronteira

$$\mathscr{L}u(x)=p_0(x)\frac{d^2}{dx^2}u(x)+p_1(x)\frac{d}{dx}u(x)+p_2(x)u(x)$$
de modo que $$<u|\mathscr{L}|u>=<u|\mathscr{L}u>=\int_a^b u(x)\mathscr{L}udx=\int_a^b u\{p_0u''+p_1u'+p_2u\}dx$$
Se exigirmos a igualdade entre a [[Integral]], exigimos
$$p_0'(x)=p_1(x)$$
Se a EDO não estiver na forma auto-adjunta, podemos multiplicar por uma função de forma a se tornar
multiplicamos por $\displaystyle \frac{1}{p_0(x)}exp\left[ \int^x \frac{p_1(t)}{p_0(t)}dt \right]$
assim, a [[EDO]] transformada em adjunta é $$\frac{1}{p_0(x)}exp\left[ \int^x \frac{p_1(t)}{p_0(t)}dt \right]\mathscr{L}u(x)=\frac{d}{dx}\left[ exp\left[ \int^x \frac{p_1(t)}{p_0(t)}dt \right]\frac{du(x)}{dx} \right]+\frac{p_2(x)}{p_0(x)}.exp\left[ \int^x \frac{p_1(t)}{p_0(t)}dt \right]u$$
multiplicamos por $\mathscr{L}$ por $f(x)/p_0(x)$ e impomos que $\displaystyle f'(x)=\frac{fp_1}{p_0}$
de modo que $$f(x)=exp\left[ \int^x \frac{p_1(t)}{p_0(t)}dt \right]$$