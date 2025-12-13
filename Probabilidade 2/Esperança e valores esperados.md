**Definição**
Seja $Z=g(x,y)$, então
$$\mathbb{E}(z)=\mathbb{E}[g(x,y)]=\begin{cases} \int\int g(x,y)f_{x,y}(x,y)dxdy,~~~~\text{caso contínuo}\\ \sum\limits_{x}\sum\limits_y g(x,y)P(X=x,Y=y),~~~~\text{caso discreto} \end{cases}$$
Alternativamente, a definição acima pode ser representada por
$$\mathbb{E}(z)=\begin{cases} \int zf_z(z)dz,~~~~\text{caso contínuo}\\ \sum\limits_z zP(Z=z),~~~~\text{caso discreto} \end{cases}$$
onde $f_z(z)$ e  a fdp de $Z=g(x,y)\to *$ 

Seja $X_1,...,X_n$ variáveis aleatórias com [[Esperança]] finita
$$\mathbb{E}(X_1+...+X_n)=\begin{cases} \mathbb{E}(X_1)+...+\mathbb{E}(X_n)\\ \int zf_z(3)dz,~~~~\text{onde z é a fdp de }Z=X_1+...+X_n \end{cases}$$
### Exemplos
**Exemplo 1**
$X_1,...,X_n$ variáveis aleatórias
1) $X_i$~Poisson($\lambda_n$), i=1,...,n
	1) $\mathbb{E}(X_i)=\mathbb{E}(X_1)+...+\mathbb{E}(X_n)=\lambda_1+...+\lambda_n$ 
2) $X_i$~$N(\mu_i,\sigma_i^2),i=1,...,n$
	1) $\mathbb{E}(X_1+...+X_n)=\mathbb{E}(X_1)+...+\mathbb{E}(X_\mu)=\mu_1+...+\mu_n$
3) X~$U(0,1)$ e Y~$U(0,1)$
	1) $\mathbb{E}(log(X)+log(Y))=\mathbb{E}(log(X))+\mathbb{E}(log(y))$
**Exemplo 2**
$X,Y$~$exp(3)$, independentes e Z=X+Y
- $\mathbb{E}(X+Y)=\mathbb{E}(X)+\mathbb{E}(Y)=\frac{1}{3}+\frac{1}{3}=\frac{2}{3}$
- $\mathbb{E}(Z)=\int zf_z(z)dz$, onde $Z$~$Gamma(2,3)$
**Exemplo 3**
$X,Y$~$U(0,1)$, independentes. $Z=X+Y$
- $\mathbb{E}(Z)=\mathbb{E}(X)+\mathbb{E}(Y)=\frac{1}{2}+\frac{1}{2}=1$
- $f_z(3)=?$


