- Também chamada de álgebra geométrica
- Generaliza conceitos de [[Vetor]]es 

Seja $\large \mathscr{v}$  um espaço vetorial de dimensão finita sobre os números reais ou seja $\mathscr{v}=\mathbb{R}^n$

Seja $\Gamma$ o conjunto de todas as combinações de até d vetores, bem como a unidade escalar 1 e a base de vetores d.
Exemplo: {1,2,....,d} => $card(\Gamma)=2^d$ 
##### [[Multivetor]]
é definido usando vetores distintos. $\gamma_{ij}$ é um multi vetor definido como
$\gamma_{ij}=\gamma_i.\gamma_j,~~~i,j\in\{1,...,d\}$ com $i\neq j$
O quadrado de vetor e multivetor são escalares denotados por $\gamma_0=1$


### Definição
A álgebra de clifford é definida no conjunto $\mathscr{G}(\mathscr{V})$ de todas as combinações lineares de escalares, vetores e multivetores derivados de $\mathscr{V}$ 
$$\mathscr{G}(\mathscr{V}) =\left\{ \sum\limits_{\lambda\in \Lambda}\alpha_\lambda\gamma_\lambda:\alpha_\lambda\in\mathbb{R},\forall\lambda\in\lambda\right\}$$
Por fim, uma álgebra de Clifford é obtida dotando G(V) com uma
operação binária associativa chamada produto de Clifford ou
geométrico.

### Produto geométrico
O produto geométrico é definido com base nos elementos da base $\gamma_1,...,\gamma_d$ de $\mathscr{V}$
$\gamma_i\gamma_j=\begin{cases}-\gamma_i\gamma_j,i\neq j\\ 1,~i=j~~e~~i=0,...,p\\ -1,~i=j~~e~~i=p+1,....,p+q\\ 0,~i=j~~e~~i=p+q+1,...,d\end{cases}$
em que $p,q\in\{0,....,d\}$ e definem a álgebra, com $p + q + r = d,$.
$Cl(p, q, r)$. Escrevemos $Cl(p, q)$ ≡ $Cl(p, q, 0)$, para r = 0.

**Exemplo**
Os [[Quatérnions]] são equivalentes a algebra $cl(0,2)$. Com
efeito, a tabela do produto de vetores e multivetores da álgebra
derivadas de um espaço vetorial de duas dimensões V cuja base
ortonormal é$\{\gamma_1,\gamma_2\}$ e $\gamma_i\gamma_j=-1$ satisfaz:

| $cl(0,2)$     | $\gamma_1$     | $\gamma_2$    | $\gamma_{12}$ |
| ------------- | -------------- | ------------- | ------------- |
| $\gamma_1$    | -1             | $\gamma_{12}$ | $-\gamma_2$   |
| $\gamma_2$    | $-\gamma_{12}$ | -1            | $\gamma_1$    |
| $\gamma_{12}$ | $\gamma_2$     | $-\gamma_1$   | -1            |
As álgebras $Cl(1, 1)$ e $Cl(2, 0)$ são isomórficas e podem ser
identificadas com os [[co-quatérnios]], também conhecidos como
[[split-quatérnios]].

| $cl(1,1)$     | $\gamma_1$     | $\gamma_2$    | $\gamma_{12}$ |
| ------------- | -------------- | ------------- | ------------- |
| $\gamma_1$    | 1              | $\gamma_{12}$ | $\gamma_2$    |
| $\gamma_2$    | $-\gamma_{12}$ | 1             | $-\gamma_1$   |
| $\gamma_{12}$ | $-\gamma_2$    | $\gamma_1$    | -1            |

| $cl(2,0)$     | $\gamma_1$     | $\gamma_2$    | $\gamma_{12}$ |
| ------------- | -------------- | ------------- | ------------- |
| $\gamma_1$    | 1              | $\gamma_{12}$ | $\gamma_2$    |
| $\gamma_2$    | $-\gamma_{12}$ | -1            | $\gamma_1$    |
| $\gamma_{12}$ | $-\gamma_2$    | $-\gamma_1$   | 1             |
