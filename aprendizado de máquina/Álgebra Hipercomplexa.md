Álgebra $\mathbb{V}$ de dimensão finita tal que existe e é único $e_0\in \mathbb{V}$ com $e_0x=xe_0=x,\forall x \in \mathbb{V}$  

**[[Álgebra não degenerada]]**
Uma álgebra $\mathbb{V}$ é dita não degenerada com respeito à base $\epsilon =\{ e_1,...,e_n \}$ se todas as formas bilineares $B_1,B_1,...,B_n$ em (4) são degeneradas. Caso contrário, a álgebra $\mathbb{V}$ é dita degenerada com respeito à base $\epsilon$


- **Produto numa álgebra $\mathbb{V}$**
$\displaystyle x = \sum\limits_{i=1}^n e_ix_i$, $y=\sum\limits_{j=1}^n y_je_j$ 
$xy=(\sum\limits_{i=1}^n e_ix_i)(\sum\limits_{j=1}^n y_je_j)=\sum\limits_{i=1}^n\sum\limits_{j=1}^n x_iy_i(\underbrace{e_j}_{\in \mathbb{V}}\underbrace{e_i}_{\in \mathbb{V}})$  com $e_ie_j\in\mathbb{V}$ com $e_ie_j\in \mathbb{V},\exists p_{ijn}$ tq
$e_je_i=\sum\limits_{k=1}^n p_{ijk}.e_k$ e podemos colocar como uma [[Matriz]] de multiplicação

**Exemplo**
- [[Números complexos]] $x=x_0+x_1i$  com a base $\epsilon =\{ 1,i \}$
Tabela de multiplicação

| Null | 1   | i   |
| ---- | --- | --- |
| 1    | 1   | i   |
| i    | i   | -1    |
- [[Quatérnios]] Base canônica $x=x_0+x_1i+x_2j+x_3k$ $\{ 1,i,j,k \}$ 
Tabela de multiplicação

| Null | 1   | i   | j   | k   |
| ---- | --- | --- | --- | --- |
| 1    | 1   | i   | j   | k   |
| i    | i   | -1  | k   | -j  |
| j    | j   | -k  | -1  | i   |
| k    | k   | j   | -i  | -1  |
- **Álgebra de dimensão 3 não hipercomplexa** Base: $\epsilon=\{ e_1,e_2,e_3 \}$

| Null  | $e_1$     | $e_2$     | $e_3$     |
| ----- | --------- | --------- | --------- |
| $e_1$ | $e_2+e_3$ | $e_3$     | $e_2$     |
| $e_2$ | $e_3$     | $e_1+e_3$ | $e_1$     |
| $e_3$ | $e_2$     | $e_1$     | $e_1+e_2$ |
**Forma bilinear**
**[[Números complexos]]** 
$$B_0=\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix},B_1=\begin{pmatrix}0 & 1 \\ 1 & 0\end{pmatrix}$$
seja $x,y\in\mathbb{C}$ 

$$\begin{bmatrix}x_0 & x_1\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix}\begin{bmatrix}y_0 \\ y_1\end{bmatrix}+\begin{bmatrix}x_0 & x_1\end{bmatrix}\begin{bmatrix}0 & 1 \\ 0 & 1\end{bmatrix}\begin{bmatrix}y_0 \\ y_1\end{bmatrix}i$$
**[[Quatérnios]]**
$$ B_0=\begin{bmatrix}1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & -1 & 0 \\ 0 & 0 & 0 & -1\end{bmatrix},~~B_1 =\begin{bmatrix}0 & 1 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & -1 & 0\end{bmatrix}, B_2=\begin{bmatrix}0 & 0 & 1 & 0 \\ 0 & 0 & 0 & -1 \\ 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0\end{bmatrix},~B_3=\begin{bmatrix}0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & -1 & 0 & 0 \\ 1 & 0 & 0 & 0\end{bmatrix}$$
**Álgebra não hipercomplexa**
$$ B_1=\begin{bmatrix}0 & 0 & 0 \\ 0 & 1 & 1 \\ 0 & 1 & 1\end{bmatrix},~B_2=\begin{bmatrix}1 & 0 & 1 \\ 0 & 0 & 0 \\ 1 & 0 & 1\end{bmatrix},~B_3=\begin{bmatrix}1 & 1 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix} $$

**[[Números Duais]]** $Z=\{ 1,i \}$

|     | 1   | i   |
| --- | --- | --- |
| 1   | 1   | i   |
| i   | i   | 0   |
$\underbrace{\begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}}_{singular},~B_1=\begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix}$
Os números duais são uma álgebra degenerada com respeito à base canônica, pois $B_0$ é singular
- Base alternativa: $\epsilon=\{ e_0,e_1 \}$, com $e_0=1+i$ e $e_1=1-i$ 
$$ \frac{e_0+e_1}{2} =1~~e~~i=\frac{e_0-e_1}{2}$$
$e_0e_0=(1+i)^2=1+2i+i^2=\frac{3}{2}e_0-\frac{1}{2}e_1$
$e_0e_1=(1+i)(1-i)=1-i^2=1=\frac{1}{2}e_0+\frac{1}{2}e_1$
$e_1e_0=\frac{1}{2}e_0+\frac{1}{2}e_1$
$e_1e_1=(1-i)^2=-\frac{1}{2}e_0+\frac{3}{2}e_1$
Nesta base a álgebra não é degenerada