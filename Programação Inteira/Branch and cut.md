
#### Algoritmo
1 --> Inicialização
Faça $\bar z=\infty, \bar z=-\infty ,x^* = \emptyset$. Coloque o problema inicial na lista $L=\{ P \}$ 

2 --> Seleção de nó

##### Exemplo
$$\begin{align}z = \max 21x_1+2x_2+31x_3+30x_4\\ s.a\begin{cases}14x_1+25x_2+14x_3+6x_4\leq 146\\ 19x_1+30x_2+24x_3+29x_4\leq 239\\ x\in \mathbb{Z}^4_+\end{cases}\end{align}$$Solução da relaxação linear no nó zero:

|       | $x_1$ | $x_3$ | $x_4$ | $f_1$   | $f_2$ | b    |       |
| ----- | ----- | ----- | ----- | ------- | ----- | ---- | ----- |
| $x_1$ | 1     | 0     | 18/7  | -131/35 | 12/35 | -1/5 | 79/35 |
| $x_2$ |       |       |       |         |       |      |       |
| z     |       |       |       |         |       |      |       |

[[Corte de Gomory]] na variável $x_1$
$\displaystyle (1-\ )$ 