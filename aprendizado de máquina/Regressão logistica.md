- A regressão logística é uma técnica de aprendizado de máquinas usada em problemas de [[Classificação binária]].
Ela é dada pela composição de um regressor
linear com a função logística.

$$f_{\theta}=\sigma \circ h_{\theta}(x)=\sigma(\theta_0+\theta_1x_1+...+\theta_nx_n)$$Em que $\sigma$ é a função logística dada por 
$$\sigma(t)=\frac{1}{1+e^{-t}}$$
```functionplot
---
title: Função phi
disableZoom: false
bounds: [-3, 3, -2, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = 1/(1+E^(-x))

```
O classificador binário fica na forma
$$\psi(x)=\begin{cases}1,~f_\theta(x)\geq0.5\\0,~\text{caso contrário}\end{cases}$$


- *Com esta função ganhamos a interpretação de probabilidade*

###### Treinamento
- o vetor de parâmetros $\theta$ podem ser determinados minimizando a entropia binária cruzada por
$$\mathcal{L}=-\frac{1}{m}\sum_{i=1}^m[y_i\log(\hat p_i)+(1-y_i)\log(1-\hat p_i)]$$
em que $\hat p_i=f_\theta(x_i)$ representa a probabilidade estimada pelo modelo de $x_i$ pertencer a classe 1 

Diferente da regressão linear e da [[Regressão Ridge]], não existe uma fórmula fechada para o [[Vetor]] dos parâmetros que minimiza a
entropia binária cruzada.

Todavia, a entropia binária cruzada é uma [[Função convexa]] e,
portanto, o mínimo da função perda $\mathcal{L}$ pode ser determinado
usando métodos de otimização como o método de máxima descida
ou o [[Gradiente]] descendente estocástico.