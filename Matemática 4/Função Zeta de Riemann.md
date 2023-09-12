A função zeta de Riemann é definida pela série
$$\zeta(s)=\sum_{n=1}^\infty \frac{1}{n^{s},}\hspace{1cm},\hspace{1cm} s\in \mathbb{C}/R_e(s)>1$$
**Convergência**
$\displaystyle \zeta(s)=\sum_{n=1}^\infty \frac{1}{n^{\Re(s)+iIm(s)}}=\frac{1}{n^{\Re(s)}}\frac{1}{n^{iIm(s)}}$ =>
$\displaystyle |\zeta(s)|= \sum_{n=1}^\infty \left|\frac{1}{n^{\Re(s)}}\right|\cdot \left|\frac{1}{n^{iIm(s)}}\right|$
Como $n^{-iIm(s)}=e^{-i(\ln(n)Im(s))}$, então $|n^{-iIm(s)}|=1$. Obtendo
$$|\zeta(s)|=\sum_{n=1}^\infty \left|\frac{1}{n^{\Re(s)}}\right|=\sum_{n=1}^\infty \frac{1}{n^{\Re(s)}}$$
que é uma [[p-série]] e portanto, converge absolutamemente para $\Re(s)>1$

### Fórmula do produto de Euler
**Teorema**
	Seja $\mathbb{P}$ o conjunto composto por todos os [[Número primo]]s. Se $\Re(s)>1$, então $\zeta(s)\neq 0$ e $$\zeta(s)=\Pi_{p\in\mathbb
	P}\left(\frac{1}{1-p^{-s}}\right)$$
	converge local e uniformemente em $\Re(s)>1$  
	**Demonstração**
	Como $|p^{-s}|=p^{-\Re(s)}<1$ para $\Re(s)>1$. Temos que a [[Série geométrica]]
	$$\left(1-\frac{1}{p^s}\right)^{-1}=\sum_{n=0}^\infty\left(\frac{1}{p^s}\right)^n=\sum_{n=0}^\infty \left(\frac{1}{p^{ns}}\right)$$
	é absolutamente convergente nesse domínio.
	Notemos que o produtório $\displaystyle \prod_{p_j}\left(1-\frac{1}{p_j^s}\right)^{-1},j=1,2,3,...,N$ 
	$\displaystyle \prod_{P_j}^{j\neq N}\left(1-\frac{1}{p^s}\right)^{-1}=\prod_{P_j}^{j\neq N}\sum_{n=0}^\infty \left(\frac{1}{P_j^{ns}}\right)$, quando abrimos a expressão
	$$\left(1+\frac{1}{2^s}+\frac{1}{2^{2s}}+\frac{1}{2^{3s}}+...\right)\left(1+\frac{1}{3^s}+\frac{1}{3^{2s}}+\frac{1}{3^{3s}}+...\right)...\left(1+\frac{1}{P_n^s}+\frac{1}{P_n^{2s}}+\frac{1}{P_n^{3s}}+...\right)$$
	Perceba que todos os denominadores do somatório final poderão ser expressos ou como um produto de primos elevado a s ou como os próprios pŕimos elevados a s. Chamaremos o conjunto que abarca esse número da base da potencia de Q
	$$\prod_{P_j}^{j\neq N}\sum_{n=0}^\infty \left(\frac{1}{P_j^{ns}}\right)=1+\frac{1}{2^s}+\frac{1}{3^{s}}+\frac{1}{4^s}+\frac{1}{5^s}+...=\sum_{m\in Q}\frac{1}{m^s}$$
	Sendo assim, o conjunto Q, representa a parte dos $\mathbb{N}$ formada pelo produto dos k-ézimos primeiros primos positivos, Assim:
	$$\left|\sum_{n=1}^\infty \frac{1}{n^s}-\sum_{m\in Q}\frac{1}{m^s}\right|\leq\sum_{n>P_n}\left|\frac{1}{n^s}\right|<\sum_{n=P_n}^\infty \left|\frac{1}{n^s}\right|=\sum_{n=P_n}^\infty \frac{1}{n^{\Re(s)}}$$
	como $\displaystyle \lim_{n \to \infty}\left[\sum_{n=P_n}^\infty \frac{1}{n^{\Re(s)}}\right]=0$, então
	$$\sum_{n=1}^\infty \frac{1}{n^s}=\lim_{n \to \infty}\left(\sum_{m \in Q}\frac{1}{m^s}\right)=\lim_{n\to\infty}\prod_{P_j}^{j\leq n}\sum_{n=0}^\infty \frac{1}{P_j^{ns}}$$=> $$\lim_{n\to \infty} \prod_{P_j}^{j\leq n}\left(1-\frac{1}{P_j^s}\right)^{-1}$$
	Assim,$$\zeta(s)=\prod_{p\in \mathbb{P}}\left(1-\frac{1}{p^s}^{-1}\right),\hspace{0.5cm}\Re(s)>1$$
	