$$P(X\geq a)\leq \frac{E[X]}{a}$$
Se X é uma [[Variável Aleatória]] que apresenta apenas valores não negativos então, para qualquer $a>0$. É válido.
**Demonstração**
Suponha que $a>0$ e $I=\begin{cases}1,~~X\geq 0\\0,~~~~c.c\end{cases}$ para tomarmos uma função apenas positiva
temos que $a.I\leq X \Rightarrow I\leq \frac{X}{a}$
$\displaystyle E[I]\leq \frac{E[X]}{E[a]}=\frac{E[X]}{a}$
sabemos que $E[I]=\int_{a}^\infty 1P(X)=P(X\geq a)$ 

**Exemplo**
Suponha que se saiba que o número de itens produzidos por uma fábrica durante uma semana seja uma variável aleatória com média $\mu=50$
1. O que se pode dizer sobre a probabilidade de que a produção desta semana seja superior a 75 itens?
Pela desigualdade de Markov,
$P(X>75) \leq \frac{50}{75}=\frac{2}{3}$ 
