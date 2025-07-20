- mede o grau de veracidade para a afirmação "O [[conjunto fuzzy]] A é igual ao conjunto fuzzy B"
**Medida de similaridade**
Uma [[Relação binária]] $\sigma_X:\mathcal{F}(X)\times \mathcal{F}(X)\to [0,1]$ simétrica é chamada relação de similaridade fuzzy em X

**Medida de similaridade Fuzzy reflexiva e forte**
Seja $\sigma_X:\mathcal{F}(X)\times \mathcal{F}(X)\to[0,1]$ uma medida de similaridade fuzzy
- Dizemos que $\sigma_X$ é reflexiva se $\sigma_X(A,A)=1~~\forall A\in \mathcal{F}(X)$
- Dizemos que $\sigma_X$ é forte se
$$\sigma_X(A,B)=1\Rightarrow A=b$$
**Teorema:** **A constinuidade implica consistência**
Sejam $\sigma_X;\mathcal{F}(X)\times\mathcal{F}(X)\to[0,1]$ uma medida de similaridade reflexiva e $\sigma_Y:\mathcal{F}(Y)\times\mathcal{F}(Y)\to[0,1]$ uma medida de similaridade forte. Considere uma base de regras fuzzy
$$\text{Se x é} ~A_i~\text{Então y é}~B_i,~~\forall i=1,...,k$$
e um [[Método de inferência disjuntivo]] ou [[Método de inferência conjuntiva]] $\psi: \mathcal{F}(X)\to \mathcal{F}(Y)$. Se $\psi$ é contínuo com respeito a base de regras, então $\psi$ é também consistente
$$\sigma_Y(\psi(A_i),B_i)\geq \sigma_X(A_i,A_i)=1\Rightarrow \psi(A_i)=B_i$$

**Definição:** [[Medida de similaridade natural]]
Seja $\mathcal{L}=([0,1],\vee,\wedge,\Delta,\to)$ um reticulado residuado. A medida de similaridade natural de $\mathcal{L}$ é o $\sigma_{\mathcal{L}}:\mathcal{F}(X)\times\mathcal{F}(X)\to[0,1]$ dada pela seguinte equação para conjuntos fuzzy $A,B\in X$
$$\sigma_{\mathcal{L}}(A,B)=\wedge_{x\in X}[A(X)\leftrightarrow B(X)]$$
em que $a\leftrightarrow b=(a\leftrightarrow b)\wedge (b\to a)$

**Teorema**
A medida de similaridade $\sigma_\mathcal{L}$ natural de um reticulado residuado $\mathcal{L}=([0,1],\vee,\wedge,\Delta,\to)$ é uma medida de similaridade reflexiva forte
**Demonstração**
Da [[Comutatividade]] do mínimo, temos
$b\leftrightarrow a=(a\leftrightarrow  b)\wedge (b\leftrightarrow  a)=a\leftrightarrow  b$
Portanto, para quaisquer $A,B\in \mathcal{F}(X)$, tem se
$$\sigma_\mathcal{L}(B,A)=\wedge_{x\in X}[B(x)\leftrightarrow A(x)]=\wedge_{x\in X}[A(x)\leftrightarrow B(x)]=\sigma_\mathcal{L}(A,B)$$
Além disso, note que
$a\leq b \leftrightarrow a\Delta 1\leq b \Leftrightarrow 1\leq a\to b \Leftrightarrow a\to b=1$
Mostraremos agora que $\sigma_\mathcal{L}(A,B)=1\Rightarrow A=B$ com efeito
$\begin{array}[t]\sigma_{A,B}=1 \Leftrightarrow \wedge_{x\in X} A(x) \leftrightarrow B(x)=1\\ \Leftrightarrow A(x)\leftrightarrow B(x)=1~~\forall x\in X\\ \Leftrightarrow (A(x)\to B(x))\wedge (B(x)\to A(x))=1,~~\forall x\in X\\ \Leftrightarrow (A(x)\to B(x))=1 ~e~(B(x)\to A(x))=1,\forall x\\ \Leftrightarrow A(x)\leq B(x) ~~e~~B(x)\leq A(x),~~\forall x\in X\\ \Leftrightarrow A(x)=B(x),~~\forall x\in X\\ \Leftrightarrow A=B\end{array}$

**Teorema**
Seja $\mathcal{L}=([0,1],\vee,\wedge,\Delta,\to)$ um reticulado residuado e defina
$$a\leftrightarrow b=(a\to b)\wedge(b\to a),~~\forall a,b\in [0,1]$$
a) $\leftrightarrow$ é uma relação de equivalência fuzzy. Em particular, tem-se
$$(a\leftrightarrow b)\Delta (b\leftrightarrow c)\leq (a\leftrightarrow c),~~\forall a,b,c\in [0,1]$$
b) Para todo $a,b,c,d\in [0,1]$, tem-se
$$(a\leftrightarrow b)\Delta (c\leftrightarrow d)\leq (a\Delta c)\leftrightarrow (b\Delta d)$$
c) Dados $a_i\in [0,1]$ e $b_i\in [0,1]$, com $i\in \mathcal{I}$, tem-se
$$\wedge_{i\in \mathcal{I}}(a_i\leftrightarrow b_i)\leq \left[(\vee_{i\in \mathcal{I}})\leftrightarrow (\vee_{i\in I} b_i)\right] $$

