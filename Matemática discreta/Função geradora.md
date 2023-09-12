**Problema fundador**
**Problema 1**
- Quantas soluções inteiras não-negativas possui a equação
$$X_1+X_2+X_3=12~~~?$$
em que $X_1\in \{2,3,4\},~X_2\in\{2,3,4\},~X_3\in\{5,6,7\}$ 
**Solução clássica**
Associado ao $x_1$ tomamos o polinômio
$P_1(x) = x^2+x^3+x^4$
$P_2(x) = x^2+x^3+x^4$
$P_3(x)=x^5+x^6+x^7$
$f(x) = P_1(x).P_2(x).P_3(x)= x^9+3x^{10}+7x^{12}+6x^{13}+3x^{14}+x^{15}$

Este índice que indica o número de soluções

**Problema 2**
Considere uma caixa com 4 bolas $\begin{cases}2~~amarelas\\1~~branca\\ 1~~cinza\end{cases}$
de quantas formas podemos retirar bolinhas desta caixa?

Considere:
$P_a(x) = 1 +ax+a^2x^2$
$P_b(x) = 1+bx$

ao multiplicarmos, temos todas as combinações possíveis


**Definição**
	Dada a sequência ($a_n$). A série será chamada de função geradora associada a sequência
	EX: $a_n = (1,1,2,0,0,0,...)$
	a função geradora é $f(x)=1+x+2x^2$

**Definição**
Se os elementos de uma [[Sequência]] ($a_n$) forem soluções de um certo problema de [[Combinação]], sua função geradora $f(x)= \sum_{n=0}^\infty a_nx^n$ é chamada de função geradora ordinária deste problema
**Propriedades**
- $\displaystyle \left( \sum_{n=0}^\infty a_nx^n\right) +\left( \sum_{n=0}^\infty b_nx^n\right)= \sum_{n=0}^\infty (a_n+b_n)x^n$
- $\displaystyle \left( \sum_{n=0}^\infty a_nx^n\right).\left( \sum_{n=0}^\infty b_nx^n\right)= \sum_{n=0}^\infty C_nx^n$ 


**Exemplo**
Escreva a função geradora ordinária do problema: de quantas formas posso selecionar n objetos de um total de N.

Seja $a_n$ a solução para n, temos $a_n= \begin{pmatrix} N\\n\end{pmatrix}$ => $f(x) = \begin{pmatrix} N\\ 0\end{pmatrix} + \begin{pmatrix} N\\1\end{pmatrix}x+\begin{pmatrix} N\\2\end{pmatrix}x^2+...+\begin{pmatrix} N\\N\end{pmatrix}x^N = (1+x)^N$

**Exemplo**
Achar a função geradora ordinária do problema determinar quantas soluções possui a equação
$$2x+3y+7n=n$$
**Exemplo**
Encontre a função geradora de $(a_n) = \begin{pmatrix} 2^n\\n!\end{pmatrix}$ 

## [[Função geradora exponencial]]
- ($a_r$) a f geradora exponencial de ($a_r$) é a  $\displaystyle f(x) =a_0 +a_1\frac{x}{1!}+a_2\frac{x^2}{2!}+...+a_r\frac{x^r}{r!}+...$
- Quando usar: Quando a ordem importar, forem objetos distintos

**Exemplo**
9 pessoas estão em uma pousada com 4 quartos marcados por tarsila, Di cavalcanti, Da vinci, Picasso.
De quantas formas estas pessoas podem se dividir nos quartos de forma que nehum fique vazio?

$(x^{0}+...+x^{7})$ => S(7,4) = $\frac{1}{4!}\left(\begin{pmatrix}4\\0\end{pmatrix}(-1)^0(4-0)^7+\begin{pmatrix}4//1\end{pmatrix}(-1)^1(4-1)^7+\begin{pmatrix}4\\2\end{pmatrix}(-1)^2(4-2)^7+\begin{pmatrix}4\\3\end{pmatrix}(-1)^3(4-3)^7 + \begin{pmatrix}4\\4\end{pmatrix}(-1)^4(4-4)^7 \right)$ = $\displaystyle \frac{1}{4!}(4^7 -4.3^7+3.2^8-4)= 350$



**Teorema**
i) O número de maneiras de distribuirmos n bolas distintas em K caixas distintas de forma que nehuma fique vazia é

ii) O número de n-úplas cujos elementos pertencem a {1,2,3,...,k} é:

A função exponencial associada é 
$\displaystyle (x+\frac{x^2}{2!}+...+\frac{x^{n-k+1}}{(n-k+1)!})^k$ 
que possui o mesmo coeficiente para $x^n/n!$ que a função
$\displaystyle g(x) = (x+\frac{x^2}{2!}+...+\frac{x^{n-k+1}}{(n-k+1)!}+...)$
Logo $\displaystyle \large g(x) = \sum_{i=0}^k \begin{pmatrix}k\\i\end{pmatrix}(-1)^{i}\underbrace{e^{k-ix}}_{\displaystyle \sum_{j=0}^\infty \frac{(k-i)^j}{j!}x^j}$
Portanto o coeficiente de $x^n/n!$ em g(x) é
$$\sum_{i=0}^k \begin{pmatrix}k\\i\end{pmatrix} (-1)^i(k-i)^n$$ 
Teorema
O número de maneiras de distribuir n bolas distintas em k caixas idênticas sem que nenhuma fique vazia é: S(n,k)= $\frac{1}{K!}T(n,k)$

**Exemplo**
De quantas maneiras podemos distribuir 4 bolas distintas a,b,c,d em duas caixas iguais, nenhuma delas ficando vazia?

Queremos calcular S(4,2) = $\frac{1}{2!}\left[ \begin{pmatrix}2\\0 \end{pmatrix}(-1)^4 (2-0)^4+\begin{pmatrix} 2\\1\end{pmatrix}(-1)^1(2-1)^4+\begin{pmatrix} 2\\2\end{pmatrix}(-1)^2(2-2)^4\right]$
 $= \displaystyle \frac{1}{2}\left[2^4+2(-1)1^4\right] = \frac{1}{2}(16-2)= 7$
 veja todas as combinações
 | Caixa 1 | Caixa 2 |
 | ------- | ------- |
 | a       | bcd     |
 | b       | acd     |
 | c       | abd     |
 | d       | abc     |
 | ab      | cd      |
 | ac      | bd      |
 | ad      | bc      |
 | cb      | ad      |
 | cd      | ab      |
 | db      | ac        |
