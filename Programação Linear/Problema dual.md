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
$$\displaystyle \begin{align}\max g(p)=b^t p\\ s.a\begin{cases}A^{tp\geq}c\\ p\geq 0\end{cases}\end{align}$$

#### Exemplo
*Problema Primal*
$\begin{align} \min z=6x_1+8x_2\\ s.a \begin{cases}3x_1+x_2\geq 4\\ 5x_1+2x_2\geq 7\\ x_1\geq 0, x_2\geq 0\end{cases}\end{align}$
*Problema Dual*
