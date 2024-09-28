
#### Teorema
Seja $\{a_n\}$ uma sequência decrescente e $\lim a_n=0$ então $\sum\limits_{n=1}^\infty (-1)^{n+1}a_n$ converge
Seja $S_n=a_1-a_2+a_3-a_4+...+(-1)^{n+1}a_n$ 
então $\underbrace{S_{2n}}_{crescente}=S_{2n-2}+\underbrace{a_{2n-1}-a_{2n}}_{>0}$         <->        $\underbrace{S_{2n+1}}_{Descrescente}=S_{2n-1}\underbrace{-a_{2n}+a_{2n+1}}_{<0}$ 

$S_2<S_4<...<S_{2n}<S_{2n-1}<...<S_1$
$\lim S_{2n}=\lim S_{2n-1}-\lim a_{2n}$

#### Teorema
Se a [[Sequência Absoluta]] de $\{a_n\}$ converge então $\{a_n\}$ converge
Seja $P_n=\begin{cases}a_n,~~a_n\geq 0\\ 0,~~a_n<0\end{cases}$ e $Q_n=\begin{cases} 0,~~a_n\geq 0\\ -a_n,~~a_n<0 \end{cases}$
$|a_n|=P_n+Q_n$; $\begin{align}P_n\geq 0\\ Q_n\geq 0\end{align}$ 
$$\begin{align}0\leq P_n\leq |a_n|\hspace{2cm} 0\leq Q_n\leq |a_n|\\ \sum\limits |a_n| ~~\text{converge}\hspace{2cm} |a_n| ~~\text{converge}\\ \sum\limits_{n=1}^\infty P_n~~\text{converge} \hspace{1,7cm} \sum\limits_{n=1}^\infty Q_n ~~\text{converge}\end{align}$$

#### Teorema
Se a sequência converge absolutamente, $b-n\neq 0$ e $\displaystyle \frac{a_n}{b_n}$ Limitada então $\{a_n\}$ converge absolutamente

$\exists C>0;~|\frac{a_n}{b_n}|\leq C~\rightarrow |a_n|\leq C|b_n|$
como $\sum\limits_{n=0}^\infty |b_n|$ converge por hipótese então $\sum\limits_{n=1}^\infty |a_n|$ converge
- **Corolário**
	Como resultado $a_n\neq 0~~\exists >0;|\frac{a_{n+1}}{a_n}|<C<1$
	para n grande. Então $\sum\limits_{n=1}^\infty a_n$ converge absolutamente


