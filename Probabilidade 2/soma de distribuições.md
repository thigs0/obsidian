X~Bernoulli (p)
Y~Bernoulli (p)
são independentes
##### Soma de [[Distribuição de Bernoulli]]
Em geral $Z=\sum\limits_{i=1}^n X_i$ ~ Binomial (np)
##### Soma de [[Distribuição normal]]
**Exemplo**
X ~ Bin (n,p) e Y ~ Bin (m,p)
Vamos mostrar Z = X + Y ~ Bin (n+m,p)

$P(Z=z)=P(X+Y=z)=\sum\limits{y=0}^m P(X+Y=z,Y=y)=\sum\limits{y=0}^z P(X=z-y,Y=y)$
$=\sum\limits{y=0}^z\begin{pmatrix}n\\ z-y\end{pmatrix}p^{z-y}(1-p)^{n-(z-y)}.\begin{pmatrix}m\\ y\end{pmatrix}p^y(1-p)^{m-y}=\left[ \sum\limits{y}^z \begin{pmatrix}n\\ z-y\end{pmatrix}  \begin{pmatrix} m\\ y \end{pmatrix}\right].p^z(1-p)^{n+m-z}=\begin{pmatrix}n+p\\z\end{pmatrix}p^z(1-p)^{n+m-z}$ 
##### Soma de [[Distribuição Gama]]
X ~ $Gama(\alpha, \lambda)$ e Y ~ $Gama(\beta,\lambda)$ independentes
Z = X + Y ~ $Gama(\alpha+\beta,\lambda)$

$f_z(z)=\int_{-\infty}^{\infty} f_x (z-y)f_y(y)dy=\int_0^\beta \frac{\lambda^{\alpha-1}}{\Gamma{x}}(z-y)^{\alpha-1}e^{-\alpha (z-y)}\frac{\lambda^{\beta-1}}{\Gamma{\beta}}y^{\beta-1}e^{-\lambda y}dy$
$=\frac{\lambda^{\lambda+\beta-z}}{P(\alpha)\Gamma(\beta)}e^{-\lambda z}\int_0^z (z-y)^{\alpha -1}y^{\beta-1}dy$ 


=> $Z=X+Y$ ~  $Gama(\alpha+\beta,\lambda)$   
De maneira geral 
$x_i,...x_n$ independentes tal que $X_i$ ~ $Gama(\alpha_i,\lambda)$, i=1,...,n
1) $z=x_1+...+x_n=\sum\limits{i=1}^n X_i$ ~ $Gama\left( \sum\limits_{i=1}^n \alpha_i,\lambda \right))$
2) $X_i$ ~ $exp(\lambda)~~i=1,...,n~~exp(\lambda)=Gama(1,\lambda)$
3) $X_i$ ~ $\xi_{v_i}^2,~~i=1,...,n$  $Z=\sum\limits_{i=1}^n X_i$ ~ $\xi_{v}^2,~~v=\sum\limits{i=1}^n v_i$


**Exemplo**
Seja $X_1,X_2$ $N(0,2),~N(1,2)$ independentes. Determine o valor de $x_0$ tq
$$P(X_1+2(X_2-1)<X_0)=0.95$$
$X_1$ ~ $N(0,2)$ => $Z=X_1+2(X_2-1)$ ~ $N(0,10)$  
$X_2$ ~ $N(0,8)$ 

normalizar e encontrarr os valores

