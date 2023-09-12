Para resolver um problema de [[Cálculo numérico/Quadrados mínimos|Quadrados mínimos]], queremos minimizar uma função perda dada por $$MSE=\min \frac{1}{m}\sum_{i=1}^m(h_\theta(x_i)-y_i)^2$$
em que $h_\theta(x)=g^t(x)\mathbf{\theta}=\theta_0+\theta_1g_1(x)+...+g_n(x)\theta_n$ com 
$\theta = (\theta_0,\theta_1,...,\theta_n)$ são os parâmetros a serem determinados e $g(1,g_1(x),g_2(x),...,g_n(x))$ são as funções que usamos para aproximar os pontos

Para realizar essa minimização, podemos usar o [[Programação Não Linear/Método do gradiente|Método do gradiente]] ou método de máxima descida

Se $$G=\begin{pmatrix}g^t(x_1)\\ g^t(x_2)\\...\\...\\g^t(x_m)\end{pmatrix}\in \mathbb{R}^{m\times (n+1)}~~e~~Y=\begin{pmatrix}y_1\\y_2\\...\\...\\y_m\end{pmatrix}\in \mathbb{R}^m$$
temos que o gradiente da função a ser minimizada é 
$$\nabla MSE=\frac{2}{m}G^t(G\theta-Y)$$
Assim, o método usa a fórmula de atualização
$$\theta_{k+1}=\theta_k-t\nabla MSE(\theta_k)$$
em que t é o passo