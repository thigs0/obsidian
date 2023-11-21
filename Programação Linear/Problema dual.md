A  todo problema de programação linear, está associado um outro problema de programação linear, chamado [[Problema dual]]
- o problema dual pode ser utilizado para resolver o problema primal


| info                 | Primal         | Dual        |
| -------------------- | -------------- | ----------- |
| Função objetivo      | Minimização -> | Maximização |
| Função objetivo      | Maximização -> | Minimização |
| Termo independente   | b          ->  | c           |
| Número de restrições | Nº Linhas  ->  | Nº Colunas  |
| Restrições |            A->    |    $A^T$         |


#### Formas equivalentes
- [[Forma canônica]]
*Primal*
$$\begin{align}\min f(x)=c^tx \\\text{s.a} \begin{cases}Ax\geq b\\ x\geq 0\end{cases}\end{align}$$
*Dual*
$$\displaystyle \begin{align}\max g(p)=b^t p\\ s.a\begin{cases}A^tp \geq c\\ p\geq 0\end{cases}\end{align}$$

#### Exemplo
*Problema Primal*
$\begin{align} \min z=6x_1+8x_2\\ s.a \begin{cases}3x_1+x_2\geq 4\\ 5x_1+2x_2\geq 7\\ x_1\geq 0, x_2\geq 0\end{cases}\end{align}$
*Problema Dual*
$\begin{align}\max v=4p_1+7p_2 \\ s.a:\begin{cases}3p_1+5p_2\leq 6\\ p_1+2p_2\leq 8\\ p_1\geq 0,p_2\geq 0\end{cases}\end{align}$

*Propriedade*: O [[Vetor]] multiplicador simplex na solução ótima primal é uma solução ótima dual
#### [[Teorema fraco da dualidade]]
Sejam $x$ uma solução factível para o problema primal e p uma solução factível para o problema dual, então $\underbrace{b^tp}_{g(p)}\leq \underbrace{c^tx}_{f(x)}$
**Demonstração**

##### Corolário 1
- Se o problema primal é ilimitado, então o dual é infactível
- Se o problema dual é ilimitado, então o primal é infactível
##### Corolário 2
Sejam $x$ e $p$ soluções factíveis dos problemas primal e dual, respectivamente, tais que $b^~tp=c^tx$. Então $x$ e $p$ são soluções ótimas dos problemas primal e dual, respectivamente
#### [[Teorema forte da dualidade]]
Se um problema de [[Programação Linear]] tem solução ótima, então seu dual também tem, e os respectivos valores ótimos são iguais

