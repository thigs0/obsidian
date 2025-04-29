- **fuzzy normal**, um [[conjunto fuzzy]] é normal se $sup_{u\in U}A(u)=1$
- **fuzzy subnormal**, um conjunto fuzzy é subnormal se $sup_{u\in U}A(u)<1$
 
- [[Suporte Fuzzy]] $Supp(A)=\{ u\in U:\varphi (u)>0 , então~~1\}$ 
- Todos os elementos que tem [[Função de pertinencia]] maior que 0

Alpha-nível são todos os pontos do [[Conjunto]] $$[A]^\alpha=\alpha-nivel(A, n)=\{ u\in U:\varphi (u)>n , então~~1\}$$ 
**Definição** de [[Cerne fuzzy]]
cerne de um conjunto fuzzy A é o subconjunto clássico de U dado por $$Cerne(A)=\{ u\in U :A(u)=1 \}$$
- Se A é subnormal, então $cerne(A)=\emptyset$ 


#### Exemplo 1
Seja $A\in \mathscr{F}(\mathbb{R})$ o conjunto fuzzy triangular caracterizado pela função de pertinência
$$A(x)=T(1,2,3)(x)=\begin{cases}x-1,1<x\leq 2\\ 3-x,2<x<3\\ 0,cc\end{cases}$$
os alpha-níveis são
$x-1<\alpha \rightarrow x<\alpha+1$ 
$3-x<\alpha\rightarrow 3-\alpha$ 
então $[\alpha+1, 3-\alpha]$

#### Exemplo 2
Determine os alpha-níveis do conjunto fuzzy $A\in \mathscr{F}([0,1])$ cuja função de pertinência é dada por
$$A(x)=4(x-x^2)$$
$4(x-x^2)>\alpha \rightarrow x^2-x+\frac{\alpha}{4}\leq 0$, usando a solução de baskara $x=\frac{1\pm \sqrt{1^2-4.1.\frac{\alpha}{4}}}{2.1}$
$[A]^\alpha=[(1+\sqrt{1-\alpha}/2), (1+\sqrt{1-\alpha})/2]$ 

#### Exemplo 3
Determine os alpha-níveis $[A]^\alpha$ do conjunto fuzzy $A\in \mathscr{F}([0,1])$ cuja função de pertinência é dada por
$$A(x)=\begin{cases} 3-x,~2<x<3\\ 0,~cc \end{cases}$$

$3-x<\alpha\Rightarrow x<3-\alpha$ como temos 0 na outra condição $[A]^\alpha =[2,3-\alpha]$

## Teorema
Considere um conjunto fuzzy $A\in \mathscr{F}(U)$. Se $0<\alpha \leq \beta\leq 1$ então$$[A]^\beta\subset [A]^\alpha$$
-o alpha-nível visto como uma função de $\alpha$ para um conjunto fuzzy A fixo, é uma operação decrescente
**Demonstração**
Considere um conjunto fuzzy A e suponha que $u\in [A]^\beta$. Pela definição de alpha-nível, a desigualdade $\alpha\leq \beta$ implica $\alpha\leq\beta A(u)$. Desse modo, novamente pela definição de alpha-nível, concluímos que $u\in [A]^\alpha$. Portanto, $u\in [A]^\beta$ implica $u\in [A]^\alpha$ ou seja,
$[A]^\beta\subset [A]^\alpha$ 

## Teorema
Qualquer conjunto fuzzy pode ser expresso em termos da função característica dos seus alpha-níveis como segue:
$$A(u)=\sup_{\alpha\in (0,1]}\alpha X_{[A]^\alpha}(u),~~\forall u\in U$$
em que $x_{[A]^\alpha}$ denota a função característica do alpha-nível, isto é
$$X_{[A]^\alpha}(u)=\begin{cases} 1,~A(u)\geq \alpha\\ 0,~A(u)<\alpha \end{cases}$$

#### Exercício
Determine os alpha-níveis do número fuzzy gaussiano limitado $G(m,\sigma, \delta)$ 

## [[Teorema de Ralescu-Negoita]]
- Condições para um intervalo ser representante de um número fuzzy
Considere uma família $\{I_\alpha :\alpha \in [0,1\}$ de intervalos fechados, limitados e não-vazios de $\mathbb{R}$ satisfazendo
1) $\displaystyle \cup_{\alpha \in (0,1]}I_\alpha =I_0$
2) Se $0\leq \alpha \leq \beta \leq 1$ , então $I_\beta\subset I_\alpha$
3) Se $\alpha_k\leq \alpha$ é uma [[Cálculo 3/Sequência|Sequência]] que converge para $\alpha \in (0,1]$, então a condição abaixo é verdadeira e existe um único [[Número fuzzy]] tal que $[A]^\alpha=I_\alpha,~\forall \alpha \in [0,1]$ 
$$\cap_{k=1}^\infty I_{\alpha k}=I_{\alpha}$$

