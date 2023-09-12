Cart (Classification and regression tree)
- Determina uma [[Árvore binária]] de decisão contruída com uma sequência de "Se...Então...Senão"
- É uma metodologia construtiva em que novo ramos são adicionados sequencialmente
- Os ramos são definidos por desigualdades em uma certa característica(Ou componentes)
Formalmente os ramos são definidos por condições da seguinte forma:
Se $x_k\leq t_k$, então ... Senão... em que $x_k$ é uma componente de uma amostra $x=(x_1,x_2,...,x_n)\in \mathbb{R}^n$ e $t_r$ é um limiar
![[cart.png|center|400]]
A componente $k$ e o limiar $t_k$ de um ramo são determinados minimizando um custo

### [[Impuridade de Gini]]
O custo é dado por $$J(k,t_k)=\frac{m_l}{m}G_{t_l}+\frac{m_r}{m}G_{t_r}$$
em que $G_l$ e $G_r$ medem a impuridade do critério e $m_l$ e $m_r$ denotam o número de amostras em cada lado da divisão
A impuridade de Gini($G_l$ ou $G_r$) é calculada pela expressão$$G=1-\sum_{i=1}^k P_i^2;~~\text{em que}~~~P_i=\frac{\# \text{amostras da classe i}}{\# amostras}$$

### Entropia
- como alternativa do índice de impuridade de Gini, pode-se usar a entropia dada por$$H=-\sum_{i=1}^kp_i\log_2p_i$$
em que k é o número de classes
- Por um lado, o índice de impuridade de Gini é mais rápido e tende a isolar classes mais frequêntes, por outro lado, a entropia tende a produzir árvores mais balanceadas

- *Regularização*
As árvores de decisão usam uma estratégia gulosa e podem sobre-ajustar o conjunto de treinamento.
para evitar o sobre-ajuste, é comum impor restrições que atuam como regularizadores Por exemplo, podemos estabelecer uma profundidade máxima da árvore
- *Complexidade computacional*
Durante o treinamento, o algoritmo efetua $O(nm\log_2m)$ 
	- vantagens e desvantagens´
		Interpretação clara dos critérios
		São extremamente sensíveis aos dados de treinamento