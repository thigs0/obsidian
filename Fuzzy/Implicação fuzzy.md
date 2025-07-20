- Satisfaz a tabela verdade clássica
- Uma implicação de [[conjunto fuzzy]] $I:[0,1]\times [0,1]\to [0,1]$ também denotada por $I(a,b)=a\to b$, decrescente no primeiro argumento e crescente no segundo é uma implicação fuzzy se satisfaz $$I(0,0)=I(0,1)=I(1,1)=1~~e~~I(1,0)=0$$

**[[Implicação de Lukasiewicz]]**
$$I_L(a,b)=1\wedge(1-a+b)=\min\{1,1-a+b\}$$
**[[Implicação de Godel]]**
$$I_M(a,b)=\begin{cases}1,~a\leq b\\ b,~c.c\end{cases}$$
**[[Implicação de Kleene-Dienes]]**
$$I_K(a,b)=(1-a)\vee b=\max\{1-a,b\}$$

**Definição:** [[Medida Subsethood]]
Uma aplicação $S:\mathcal{F}(U)\times \mathcal{F}(U)\to [0,1]$ é uma medida de subsethood se satisfaz
1) $S(A,B)=1~~se~~A\subset B$
2) $A(U,\emptyset)=0$
3) Se $A\subset B\subset C$ então $S(C,A)\leq S(B,A)$ e $S(C,A)\leq S(C,B)$
E podem ser definidas como 
$$S^\cap(A,B)=\begin{cases} 1,~~A=\emptyset\\ \frac{card(A\cap B)}{Card(A)} ,~~c.c\end{cases}$$
$$S^\cup(A,B)=\begin{cases} 1,~~A\cup B=\emptyset\\ \frac{Card(B)}{Card(A\cup B)} ,~~c.c\end{cases}$$
###### Exemplo
$A=\{ 1,2,3 \},~~B=\{ 1,2,4,5 \}~~e~~C=\{4,5,6\}$ então $$\begin{align}S^\cap(A,B)=2/3~~e~~S^\cap(A,C)=0\\ S^\cup(A,B)=4/5~~e~~S^\cap (A,C)=1/2\end{align}$$

