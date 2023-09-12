Um classificador é uma função $\Psi;X\to C$, em que X é o espaço
das características ou entradas e C é o conjunto das classes ou
rótulos.
- Na [[Classificação binária]], os [[Conjuntos]] das classes possui apenas dois elementos, ou seja, Card(C) = 2.
Este mesmo conjunto pode ser identificado de várias formas
$$\begin{align} C=\{c_0,c_1\}\\ C=\{0,1\}\\ C=\{-1,1\}\end{align}$$

**Acurácia para um classificador binário**
- Podemos utilizar a [[Acurácia]] para avaliar o desempenho de um classificador binário.ψ : X → {0, 1}
$$\psi (x)\to\{0,1\}$$
$$\text{Acurácia}=\frac{1}{m}\chi[y_k=\psi(x_k)]$$
em $$\chi[s]=\begin{cases}1,~\text{s é verdadeiro}\\ 0,~\text{caso contrário}\end{cases}$$
