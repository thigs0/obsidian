- uma informação que quantifica um valor
- Descreve um número real e seu entorno tal que todos seus [[alpha-nível]] são intervalos fechados, limitados e não-vazios denotadas por $\mathbb{R}_f$
- $[A]^\alpha=[a_1^\alpha, a_S^\alpha],~\forall \alpha \in [0,1]$ em que $a_1^\alpha$ e $a_S^\alpha$ corersponde, respectivamente ao extremo inferior e superior do intervalo

#### [[Função de pertinência trapezoidal]]
### [[Função de pertinência triangular]]

### [[função de pertinência Gaussiano limitado]]
$$G(m,\sigma,\delta)=\begin{cases}e^{-(x-m)^2/\sigma^2},~x\in [m-\sigma,m+\sigma]\\ 0,~~\text{caso contrário}\end{cases}$$

## [[teorema de Ralescu-Negoita]]
Considere uma família $I_\alpha:\alpha\in[0,1]$ de intervalos fechados, limitados e não-vazios de $\mathbb{R}$ 
1) $\overline{ \cup_{\alpha \in (]0,1} I_\alpha}=I_0$ 
2) Se 


### Operação intervalar
Sejam $A=[a_I,a_S]$ e $B=[b_I,b_S]$ intervalos fechados, então:
1) $A+B=[a_I+b_I,a_S+b_S]$
2) $A-B=[a_I-b_S,a_S-b_I]$ 
3) $A.B=[\min P,\max P]$, em que $P=\{ a_Ib_I,a_Ib_S,a_Sb_I,a_Sb_S \}$
4) $A/B=[a_I,a_S].\left[ \frac{1}{b_S},\frac{1}{b_I} \right]$ se $0\notin B$ 
**Exemplo**
Determine A+B,A-B,A.B e A/B para os intervalos fechados $A=[-1,2]$ e $B=[5,6]$
$$\begin{align*}A+B=[-1+5,2+6]=[4,8]\\ A-B=[-1-6,2-5]=[-7,-3]\\ A.B=[\min A,\max A],A=\{-1.5, -1.6,2.5,2.6\}= [-6, 12]\\ A/B=[-1,2].[\frac{1}{6},\frac{1}{5}]=\left[ -\frac{1}{6} ,\frac{2}{5}\right]\end{align*}$$
#### Operação fuzzy
Sejam A e B números fuzzy e * uma operação aritmética para intervalos fechados. O número fuzzy $A*B$ é definido de modo que $$[A*B]^\alpha =[A]^\alpha*[B]^\alpha,~~\forall \alpha \in [0,1]$$
Como $[A]^\alpha$ e $[B]^\alpha$ são intervalos fechados, $[A]^\alpha*[B]^\alpha$ é também um intervalo fechado
- sobretudo $[A*B]^\alpha$ satisfaz as condições de [[Ralescu-Negoita]] 
**Exemplo**
Determine A+B para os números fuzzy triangulares $A=T(-1,1,3)$ e $B=T(1,3,5)$
Temos $[A+B]^\alpha  =[4\alpha ,8-4\alpha],~\forall \alpha \in [0,1]$
os números triangulares $$A=\begin{cases}\frac{x}{2}+\frac{1}{2},~~-1<x<1\\- \frac{x}{2}-\frac{3}{2},~~1<x<3\\ 0,~~c.c\end{cases};~~B=\begin{cases}\frac{x}{2}-\frac{1}{2},~~1<x<3\\ -\frac{x}{2}+\frac{5}{2},~~ 3<x<5\\ 0,~~c.c\end{cases}$$
$$[A]^\alpha= \begin{align*} \frac{x}{2}+\frac{1}{2}<\alpha \Rightarrow x<2\alpha-1\\ \frac{-x}{2}+\frac{3}{2}<\alpha \Rightarrow x>-2\alpha +3 \end{align*}\Rightarrow [2\alpha-1, -2\alpha +3]$$
$$[B]^\alpha=\begin{align*} \frac{x}{2}-\frac{1}{2}<\alpha \Rightarrow x<2\alpha +1\\ \frac{-x}{2}+\frac{5}{2}<\alpha \Rightarrow x>-2\alpha +5 \end{align*}\Rightarrow [2\alpha +1],-2\alpha +5]$$
Então $[A+B]^\alpha =[2\alpha+1+2\alpha-1, -2\alpha+5-2\alpha +3]=[4\alpha,8-4\alpha]$ 

e por fim temos $A+B=T(0,4,8)$