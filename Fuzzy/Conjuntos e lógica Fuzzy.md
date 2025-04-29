
**Fuzzy** pode significar algo incerto, subjetivo

[[Princípio da incompatibilidade de zadeh]]
...


**[[Função de pertinencia]]**
Considerando o universo clássico de [[Conjuntos]], temos uma função que constroi uma transição gradual
$$\varphi_A:U \rightarrow [0,1]$$
***caracteristicas***
1) $\varphi_\emptyset (x)=0$ , todos os elementos estão fora do conjunto
2) $\varphi_U(x)=1$, todos os elementos estão no conjunto
3) $A=B \Rightarrow \varphi_A(x)=\varphi_B(x)$, Se dois conjuntos Fuzzy são iguais, sua funções de pertinencia são iguais 

**[[Função de pertinência triangular]]**
$$T(a,m,b)(x))$$

**[[Função de pertinência trapezoidal]]**
$$T(a,m,n,b)(x)=\begin{cases}(x-1)/(m-1), ~a<x<m\\ 1\\ (b-x)/(b-n), ~n<x<b\\ 0 ~ C.C\end{cases}$$

**[[Função de pertinência de Cauchy]]**
$$\displaystyle C(a,b,c)(x)=\frac{1}{1+|\frac{x-c}{a}|^{2b}}$$
### Função  de pertinência gaussiana limitada
$$G(x,\sigma,\delta)=\begin{cases} \exp \left( \frac{(x-\delta)^2}{2\sigma^2} \right),~a\leq x\leq b\\ 0.~~cc \end{cases}$$

### Operações em conjunto Fuzzy

**[[Intersecção]]** $\varphi_{A\cap B}(x)=\mathscr(\varphi_A ...)$

**[[União]]** $A\cup B=\mathscr{D}(A(x),B(x))), \forall x\in U$


**[[Complemento]]** 