A regressão lasso, do inglês (least absolute shrinkage and selection operator), é obtida adicionado ao MSE a soma dos valores absolutos dos parâmetros $\theta_1,\theta_2,...,\theta_n$
Esta regressão modifica a formulação do [[Cálculo numérico/Quadrados mínimos|Quadrados mínimos]] assim como a [[Regressão Ridge]]. De forma que temos
$$\min \frac{1}{2m}\sum_{i=1}^m (H^t\theta-y_i)^2+\alpha\sum_{j=1}^n |\theta_j|$$
- A regressão lasso tende à eliminar os parâmetros associados às características menos importantes. Dessa forma, ela pode ser usada para seleção de características.
- A função a ser minimizada não tem [[Derivada]], ainda assim usamos o [[Subgradiente]] para encontrar a solução visto que a função é uma [[Função convexa]]