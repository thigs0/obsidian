A Elastic Net combina os termos de regularização da [[Regressão Lasso]] e [[Regressão Ridge]], resultando na [[função]] perda
$$\min \frac{1}{2m}\sum_{i=1}^m (H^t\theta-y_i)^2+(1-r)\frac{\alpha}{2}\sum_{j=1}^n |\theta_j|+r\alpha\sum_{i=1}^n|\theta_i|$$
Para $\alpha\geq 0$ e $0\leq r\leq 1$
- Quando $r=0$ temos a [[Regressão Lasso]]
- Quando $r=1$ temos a [[Regressão Ridge]]
- Recomendado quando o número de características é maior do que as amostras
-  a elastic net pode apresentar resultados melhores que a regressão lasso quando o número de características é maior que o número de amostras $(n > m)$ ou existem muitas características fortemente relacionadas.

![[regressão.png|center|450]]
Vemos que a regressão ElastcNet apresenta o mesmo comportamento da [[Regressão Lasso]] com um desvio para a [[Regressão Ridge]]
