- baseado no método simplex


**Criamos  a tabela inicial**

|     | $x^t$ |     |
| --- | ----- | --- |
|   base  | $c^t$ |    -f(x) |
| $x_b$    | A     | b   | 

**Exemplo**
$$\begin{align}\min -3x_1-2x_2+0x_3+0x_4+0x_5\\ s.a\begin{cases} 0.5x_1+0.3x_2+x_3=3\\ 0.1x_1+0.2x_2+x_4=1\\0.4x_1+0.5x_2+x_5=3\\ x_1,x_2,x_3,x_4,x_5\geq 0 \end{cases}\end{align}$$
criando a tabela

|       | $x_1$ | $x_2$ | $x_3$ | $x_4$ | $x_5$ |     |
| ----- | ----- | ----- | ----- | ----- | ----- | --- |
| Base  | -3    | -2    | 0     | 0     | 0     | 0   |
| $x_3$ | 0.5   | 0.3   | 1     | 0     | 0     | 3   |
| $x_4$ | 0.1   | 0.2   | 0     | 1     | 0     | 1   |
| $x_5$ | 0.4   | 0.5   | 0     | 0     | 1     | 3   |

**Iteração 1**
vemos que $x_1$ tem o menor custo relativo
Faremos o teste da razão
$\displaystyle \frac{3}{0.5}=6$
$\displaystyle \frac{1}{0.1}=10$ ; O menor é 6
$\displaystyle \frac{3}{0.4}=7.5$ 

Vamos pisotear o encontro entre a linha com o menor valor e a coluna com o menor valor que é $0.5$. Vamos deixar este valor 1 e a linha abaixo dele com 0

Nova tabela multiplicamos a linha por 2 até ficar um
Na segunda por $-0.1l_1$
Na terceira por $-0.4l_1$

|       | $x_1$ | $x_2$ | $x_3$ | $x_4$ | $x_5$ |      |
| ----- | ----- | ----- | ----- | ----- | ----- | ---- |
| Base  | -3    | -2    | 0     | 0     | 0     | 0    |
| $x_3$ | 1     | 0.6   | 2     | 0     | 0     | 6    |
| $x_4$ | 0     | 0.14  | -0.2  | 1     | 0     | 0.4  |
| $x_5$ | 0     | 0.3   | -0.08 | -0.4  | 1     | 2.84 |
