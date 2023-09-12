É o método dos [[Cálculo numérico/Quadrados mínimos|Quadrados mínimos]], porém com termos 
- A regressão ridge utiliza a chamada regularização de Tikhonov

$$\min \frac{1}{m}\sum_{i=1}^m (H^t\theta-y_i)^2+\alpha\sum_{j=1}^n \theta_j^2$$
Em que $H$ é o vetor das das funções que aproximam calculados nos pontos do vetor $\mathbf{x}$ e $\alpha \geq 0$ 
- Caso $\alpha =0$, obtemos a regressão linear usual
- Quando $\alpha$ é muito grande, os parâmetros de $\theta$ tendem a 0
- A formulação penaliza parâmetros muito grandes que podem causar overfitting

**Código da regressão ridge em python**

```python
import micropip 
await micropip.install('numpy',keep_going=True)
await micropip.install("matplotlib")
await micropip.install('scikit-learn')
import numpy as np 
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression, Ridge, Lasso, ElasticNet
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import Pipeline
from sklearn.metrics import mean_squared_error, mean_absolute_error

#Gerando dados com ruído para reta y=0.5x^2+x+2
np.random.seed(42) # to make this code example reproducible
m = 30
X = 6 * np.random.rand(m, 1) - 3
y = 0.5 * X**2 + X + 2 + np.random.randn(m, 1)

Xtr, Xte, ytr, yte = train_test_split(X, y, test_size = 0.5, random_state=42) # Separamos os dados de treinamento

#Regressão linear a regressão rifge
p10_usual = Pipeline((
("poly_features", PolynomialFeatures(degree=10, include_bias=False)),
("linear_reg", LinearRegression()),)
).fit(Xtr,ytr)

p10_ridge = Pipeline((
("poly_features", PolynomialFeatures(degree=10, include_bias=False)),
("ridge_reg", Ridge(alpha=1.0)),)
).fit(Xtr,ytr)

reg_list = [("Tradicional",p10_usual), ("Ridge",p10_ridge)]
for reg in reg_list:
    print("Regressão ",reg[0])
    print("Polinomio: %2.2f+%2.2f x+%2.2f x^2 + %2.2f x^3 + %2.2f x^4 + %2.2f  x^5 +%2.2f x^6+%2.2f x^7+%2.2f x^8+%2.2f x^9+%2.2f x^{10}" 
          % (reg[1][1].intercept_,
             reg[1][1].coef_.flatten()[0],
             reg[1][1].coef_.flatten()[1],
             reg[1][1].coef_.flatten()[2],
             reg[1][1].coef_.flatten()[3],
             reg[1][1].coef_.flatten()[4],
             reg[1][1].coef_.flatten()[5],
             reg[1][1].coef_.flatten()[6],
             reg[1][1].coef_.flatten()[7],
             reg[1][1].coef_.flatten()[8],
             reg[1][1].coef_.flatten()[9]))
    print("---")
```