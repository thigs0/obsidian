- Definição, A integral dupla de f sobre o retângulo R é:
$$\left| \iint_R f(x,y)dA-\sum\limits_{i=1}^m \sum\limits_{j=1}^n f(x_{ij}^*, y_{ij}^*)\Delta A\right|<\epsilon$$
- soma dupla de Riemann

**A regra do ponto médio**
usamos o ponto médio para aproximar as funções
$$\iint_R f(x,y)dA \approx \sum\limits_{i=1}^m\sum\limits_{j=1}^n f(\bar x_i, \bar y_j)\Delta A$$
**valor médio**
- Para $f(x)$
$$f_{med}=\frac{1}{b-a}\int_{a}^b f(x)dx$$
- Para duas variáveis
$$f_{med}=\frac{1}{\underbrace{A(R}_{\text{Área de R}})}\iint f(x,y)dA$$

**Propriedades**
- (propriedades da soma) $\displaystyle \iint_R [f(x,y)+g(x,y)]dA=\iint_R f(x,y)dA+\iint_R g(x,y)dA$
- (propriedade da constante) $\displaystyle \iint_R cf(x,y)dA =c\iint_R f(x,y)dA$, c é constante
- (se $f(x,y)\geq g(x,y)$) $\displaystyle \iint_R f(x,y)dA \geq \iint_R g(x,y)dA$


#### [[Teorema de Fubini]]
$R=\{ (x,y)|a\leq x\leq b, c\leq y\leq d\}$, então
$$\iint_R f(x,y)dA=\int_a^b\int_c^d f(x,y)dydx = \int_c^d\int_a^b f(x,y)dxdy$$

