Sejam A e B conjunto não vazios. Uma função de A em B é uma associação entre os elementos de A e B, de maneira que todo elemento em A está associado a um único elemento de B
$$f:A \rightarrow B$$
A é o domínio 
B é o contradomínio

**[[Função injetora]]**
Elementos distintos, levam até funções distintas
$f:A \rightarrow B$, $x \in A$ -> $f(A) \neq f(b)$

**Contrapositiva**
$a \in A,~b \in B$; $f(a)=f(b) \Rightarrow a=b$

**[[Função sobrejetora]]**
Para todo $b \in B$ existe $a \in A$ tal que $f(a)= b$
$f:A \rightarrow B$ 
Im(f) = {$b \in B$} Existe $a \in A$ tal que f(a) = b c B

_Exemplo_
$f(x) = 3x-2$ é sobrejetora
$b \in \mathbb{R}$ tome $a = \frac{b+2}{3}$
f(x) = 3x-2 -> f(a) = 3a-2 -> f($\frac{b+2}{3}$) =3 $\frac{b+2}{3}-2=b$

**[[Função unívoca]]**
Uma função é unívoca se $f(a)\neq f(b)$ sempre que $a \neq b$. com $f(a)=b \neq f(b)=a$

**[[Função inversa]]**
Para uma função qualquer f, denominamos inversa de f, e denotamos $f^{-1}$, são os [[Conjuntos]] de todos os pares (a,b) para os quais o par (b,a) pertence a f
-> $f^{-1}$ é uma função se, f é unívoca
-> Troca x e y de lugar na função. Após, isole o y e tera a função inversa

---
#### Operação com funções
***Soma de funções***
$(f+g)(x)=f(x)+g(x)$
- O domínio de f+g e $Dom(f+g)=Dom(f)\cap Dom(g)$
***Produto de funções***
$(f.g)(x) = f(x).g(x)$
- Domínio de f.g é $Dom(f.g)=Dom(f)\cap Dom(g)$
***Quociente de funções***
$\displaystyle \left(\frac{f}{g}\right)(x)=\frac{f(x)}{g(x)}$ 
- O domínio é $Dom(f) \cap Dom(g) \cap \{x|g(x)\neq 0\}$
***Composição de funções***
$(f \circ g)(x)=f(g(x))$
- é associativo $(f \circ g)\circ h=f\circ (g\circ h)$

---

```functionplot
---
title: Função Seno(x),seno^2(x), seno(x^2)
disableZoom: false
bounds: [-1, 3, -2, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = sin(x)
g(x) = (sin(x))^2
h(x) = sin(x^2)

```
