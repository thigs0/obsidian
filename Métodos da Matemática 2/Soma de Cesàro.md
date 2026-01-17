A soma de Cesàro ou [[média C-1]] como a média aritmética de somas parciais
$$\sigma_n(x)=\frac{1}{N}\sum\limits_{k=0}^{N-1} S_k(x),~~N=1,2,...$$
e $$S_n(x)=\sum\limits_{n=0}^k u_n(x),~~~k=0,1,2,...,N-1$$
A [[série]] é C-1 Somável se existir N -> $\infty$ de $\sigma_N(x)$. Então
$\displaystyle \sigma_N(x)=\frac{1}{N}\sum\limits_{k=0}^{N-1} \underbrace{S_k(x)}_{\sum\limits_{n=0}^k u_n(x)}=  \frac{1}{N}\sum\limits_{k=0}^{N-1} \sum\limits_{n=0}^k u_n(x)=\frac{1}{N}\sum\limits_{n=0}^{N-1}\sum\limits_{k=n}^{N-1}u_n(x)$
Observação: $\sum\limits_{k=n}^{N-1}1 = (N-1)-n=N-n$
$\sigma_N(x)=\frac{1}{N}\sum\limits_{n=0}^{N-1}\underbrace{\sum\limits_{k=n}^{N-1}u_n(x)}_{\text{constante em n}}=\frac{1}{N}\sum\limits_{n=0}^{N-1} (N-n)u_n =\sum\limits_{n=0}^{N-1} \left(1-\frac{n}{N}\right)u_n(x)$
A [[série]] é C-2 Somável se existir N -> $\infty$ de $\sigma_N(x)$. Então

$\sigma_N^{(2)}(x)=\frac{1}{N}\sum\limits_{n=0}^{N-1} \sigma_k(x)$ 


