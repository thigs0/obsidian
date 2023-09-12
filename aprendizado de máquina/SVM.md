- Uma máquina de suporte (SVM) linear, para classificação, define uma função $$\Psi (x)=\begin{cases}1 ~~~h(s)\geq 0\\ -1 ~\text{Caso contrário}\end{cases}$$
Em que a função de decisão é
$$h(x)=\omega^t x+b$$
Os parâmetros $\omega \in \mathbb{R}^n$ e $b\in \mathbb{R}$ são determinados pelo [[Hiperplano]] que maximiza a margem de separação entre as amostras de classes distintas.
Formalmente $\omega$ e $b$ são soluções do problema de otimização quadrática(primal)

$$\min \frac{1}{2}\omega^t\omega +\frac{c}{m}\sum_{i=1}^n \xi_i$$
$$s.a:\begin{cases} y_i(w^tx_i+b)\geq 1-\xi_i\\ \epsilon\geq0,~\forall i=1,2,3,...,m \end{cases}$$
de forma equivalente, temos o problema de otimização quadrática(dual)
$$\max \sum_{i=1}^m \alpha_i-\frac{1}{2}\sum_{i=1}^m \sum_{j=1}^m \alpha_i\alpha_jy_iy_jx_i^tx_j$$
$$s.a:\begin{cases}\sum_{i=1}^m \alpha_iy_i=0\\ 0\leq \alpha_i\leq\frac{c}{m}\end{cases}$$
Os multiplicadores são nulos para a maioria dos índices. Sendo $\alpha_i>0$ somente nos vetores de suporte
Conhecendo os multiplicadores $\alpha_1,\alpha_2,...,\alpha_m$ podemos calcular $w$ usando a equação$$w=\sum_{i=1}^m \alpha_iy_ix_i$$
