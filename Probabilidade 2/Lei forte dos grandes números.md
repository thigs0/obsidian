Se $X_1,X_2,...$ uma [[Cálculo 3/Sequência|Sequência]] de [[Variável Aleatória]] independentes e identicamente distribuídas, cada uma com média finita $\mu=\mathbb{E}[X_i]$. Então, com probabilidade 1
$$\frac{X_1+X_2+...+X_n}{n}\to \mu~~~~quando~~~~n\to\infty$$
Como uma aplicação da lei forte dos grandes números, suponha que seja realizada uma sequência de tentativas independentes de um experimento. Suponha que $\mathbb{E}$ seja um evento fixo do experimento e que $P(E)$ represente a probabilidade de que $E$ ocorra em qualquer tentativa particular. fazendo
$$X_i=\begin{cases}1~~\text{Se E ocorrer na i-ésima tentativa}\\ 0~~\text{Se E não ocorrer na i-ésima tentativa}\end{cases}$$
temos, pela lei forte dos grandes números, que, com probabilidade 1
$$\frac{X_1+...+X_n}{n}\to \mathbb{E}[X]=P(E)$$
Como $X_1+...+X_n$ representa o número de vezes em que o evento $E$ ocorre nas primeiras n tentativas, podemos interpretar a equação como se ela dissesse que, com probabilidade 1, a proporção limite do tempo de ocorrência do evento $E$ é justamente $P(E)$
Embora o teorema possa ser demonstrado sem essa hipótese, nossa demonstração da lei forte dos grandes números supõe que as variáveis aleatórias X, possuem um quarto momento finito. Isto é, supomos que $\mathbb{E}[X_i^4]=K<\infty$
