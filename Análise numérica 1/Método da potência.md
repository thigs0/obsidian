- Método que tenta aproximar o [[Autovetor]] e [[Autovalor]] associados à uma [[Matriz]]
Para este método, supomos que a matriz $A \in \mathbb{R}^{(n_xn)}$ tenha n  autovalores $\lambda_1, \lambda_2,...,\lambda_n$ com n autovetores associados $v^{(1)}, v^{(2)},...v^{(n)}$Supomos ainda que $|\lambda_1|>|\lambda_2|>...>|\lambda_n|\geq 0$ 
Seja x um vetor arbitrário de $\mathbb{R}^n$. Como os autovetores são perpendiculares. Podemos reescrever x como Combinação linear
$$x=\sum_{i=1}^n \beta_iv^{(i)}$$
Temos que A é Diagonalizável, então tamos que
$$A^{k}x=\sum_{i=0}^n\lambda_i^k\beta_iv^{(i)}\Rightarrow A^kx=\lambda_1^k\sum_{i=1}^n\beta_i\left( \frac{\lambda_j}{\lambda_1}\right)^kv^{(i)}$$
Como temos $|\lambda_1|$ sendo maior que os outros, o seguinte [[Limite]] tende à 0
$\displaystyle \lim_{k \to \infty} \left(\frac{\lambda_j}{\lambda_1}\right)^k=0$ 
Assim a sequência $\begin{cases}|\lambda_1|>1 \rightarrow ~~Diverge\\ |\lambda_1|<1 \rightarrow ~~Converge\end{cases}$




#### **Algoritmos**
x <- aproximação inicial do autovetor
A <- Matriz
n <- Número de iterações
**Para i de 1 até n**
	$y = Ax$
	$\mu = \|y\|_\infty$ 
	$p = \text{Valor de y cuja norma infinita seja máxima}$ 
	$x=y/p$ , esse p conta o sinal do elemento que gerou 

***Exemplos*** 
Encontre o maior autovalor e o autovetor associado de A, com $x^{(0)}$ inicial.
$A=\begin{pmatrix}-4 & 14 & 0 \\ -5 & 13 & 0 \\ -1 & 0 & 2\end{pmatrix}$ e $x^{(0)}=\begin{pmatrix}1 \\ 1 \\ 1\end{pmatrix}$
Encontramos $Ax$
$y=Ax=\begin{pmatrix}-4 & 14 & 0 \\ -5 & 13 & 0 \\ -1 & 0 & 2\end{pmatrix}\begin{pmatrix}1 \\ 1 \\ 1 \end{pmatrix}= \begin{pmatrix}10 \\ 8 \\ 1\end{pmatrix}$
Agora, encontramos $\mu$ que é a aproximação do autovalor
$\mu = \max(|10|, |8|, |1|)=10$ e $p=10$
Portanto, nossa primeira aproximação para o autovetor é 
$x = \begin{pmatrix}10 \\ 8 \\ 1\end{pmatrix}/10=\begin{pmatrix}1 \\ 0.8 \\ 0.1\end{pmatrix}$
Uma segunda iteração
$y=Ax=\begin{pmatrix}-4 & 14 & 0 \\ -5 & 13 & 0 \\ -1 & 0 & 2\end{pmatrix}\begin{pmatrix}1 \\ 0.8 \\ 0.1\end{pmatrix}=\begin{pmatrix}7.2 \\ 5.4 \\ -0.8\end{pmatrix}$
$\mu = max(|7.2|, |5.4|, |-0.8|)=7.2$ e $p=7.2$
então
$x=y/7.2=\begin{pmatrix}1 \\ 0.75 \\ -0.11\bar{1}\end{pmatrix}$ 

**Python**
```python
import numpy as np
import matplotlib.pyplot as plt
import scipy.linalg as la

def powervalor(A, v):
	Av = A.dot(v)
	return v.dot(Av)
def power_iteracao(A):
	n, d = A.shape
	v = np.ones(d) / np.sqrt(d)
	ev = powervalor(A, v)
	while True:
		Av = A.dot(v) 
		v_new = Av / np.linalg.norm(Av) 
		ev_new = powervalor(A, v_new) 
		if np.abs(ev - ev_new) < 0.0001:
			break
		v = v_new ev = ev_new 
		return ev_new, v_new
```

---

#### Técnica da deflação
**Ideia**: Formar uma [[matriz]] B que tenha os mesmos autovalores de A, com exceção do autovalor dominante de A, que será substituído por 0 em B.

##### **Teorema**
Suponha que $\lambda_1, \lambda_2,...\lambda_n$ sejam autovalores de A com autovetores associados $v^{(1)}, v^{(2)}, ...,v^{(n)}$ e $\lambda_1$ tenha multiplicidade 1. Seja x um vetor tal que $x^tv^{(1)}=1$. Então, a matriz 
$$B=A-\lambda_1v^{(1)}x^t$$
Tem autovalores $0, \lambda_2, \lambda_3, ...,\lambda_n$ com autovetores associados $v^{(1)}, w^{(2)},w^{(3)},...,w^{(n)}$, onde $v^{(i)}$ e $w^{(i)}$ são relacionados pela equação
$$v^{(i)}=(\lambda_i-\lambda_1)w^{(i)}+\lambda_1(x^tw^{(i)})v^{(1)}$$
para cada i=2,3,4,...,n
###### **Demonstração**
 temos que $Bv^{(1)}=(A-\lambda_1v^{(1)})x^t)v^{(1)}=Av^{(1)}-\lambda_1v^{(1)}\underbrace{x^tv^{(1)}}_{1}=Av^{(1)}-\lambda_1v^{(1)}=0$ 
 Portanto 0 é autovalor de B, com [[Vetor]] associado ao autovetor $v^{(1)}$ 
 Agora $Av^{(i)}=\lambda_iv^{(i)}$ para $i\neq1$ temos:
 $$\large A[\underbrace{(\lambda_i-\lambda_1)w^{(i)}+\lambda_1(x^tw^{(i)})v^{(1)}}_{v^{(1)}}]=\lambda_i[\underbrace{(\lambda_i-\lambda_1)w^{(i)}+\lambda_1(x^tw^{(i)})v^{(1)}}_{v^{(i)}}]$$
 $\displaystyle \large =A(\lambda_i-\lambda_1)w^{(i)}+\lambda_1Ax^tw^{(i)}v^{(1)}=\lambda_i(\lambda_i-\lambda_1)w^{(i)}+\lambda_i\lambda_1(x^tw^{(i)})v^{(i)}$ 


----
###### [[Deflação de Wielandt]]
Há muitas escolhas de vetor x no teorema anterior. Aqui vamos usar o processo de deflação de Wielandt no qual x é definido por $$x=\frac{1}{\lambda_1v_i^{(1)}}(a_{i1},a_{i2},...,a_{in})^t$$
onde $v_i^{(1)}$ é uma coordenada diferente de zero do autovetor $v^{(1)}$ e $(a_{i1},a_{i2},...,a_{in})$ é a i-ésima linha de A
Definindo-se assim, temos
$$x^tv^{(1)}=\frac{1}{\lambda_iv_i^{1}}\sum_{j=1}^n a_{ij}v_j^{(1)}$$
Como $Av^{(1)}=\lambda_1v^{(1)}$, então $\sum_{j=1}^n a_{ij}v_j^{(1)}=\lambda_iv_i^{(i)}$.
Logo $x^tv^{(1)}=1$. Ou seja, x definido acima satisfaz as hipótese do teorema. Além disso, a i-ésima linha de $B=A-\lambda_1v^{(1)}x^t$ consiste inteiramente em entradas iguais a zero
**Obs**
1. A i-ésima linha de $B=A-\lambda_1v^{(1)}x^t$, $x=\frac{1}{\lambda_1v_i^{(1)}}(a_{i1},...a_{in})^t$ consiste inteiramente em entradas iguais a zero
2. Se $\lambda \neq 0$ é um autovalor com autovetor associado w, a relação $Bw=\lambda w$ implica que a i-ésima coordenada de w deve ser zero. Consequentemente, a i-ésima coluna de B também não contribuiu para o produto $Bw=\lambda w$ 
3. Este método apresenta muitos erros de arredondamento

***Exemplo***
$A=\begin{pmatrix}4 & -1 & 1 \\ -1 & 3 & -2 \\ 1 & -2 & 3\end{pmatrix}$ Encontramos o primeiro auto valor e seu autovetor
$\lambda_1=6$, $v^{(1)}=\begin{pmatrix}1 \\ -1 \\ 1\end{pmatrix}$
Encontramos o x
$x=\frac{1}{\lambda_1v_1^{(1)}}A_1^t=\frac{1}{1*6}\begin{pmatrix}4 \\ -1 \\ 1\end{pmatrix}=\begin{pmatrix}2/3 \\ -1/6 \\ 1/6\end{pmatrix}$

Com isso, conseguimos encontrar nossa matriz B
$B=A-\lambda_1v^{(1)}x^t=A-6\begin{pmatrix}1 \\ -1 \\ 1\end{pmatrix}\begin{pmatrix}2/3 & -1/6 & 1/6\end{pmatrix}$
$B=\begin{pmatrix}0 & 0 & 0 \\ 3 & 2 & -1 \\ -3 & -1 & 2\end{pmatrix}$
Removendo a primeira linha e a primeira coluna
$B'=\begin{pmatrix}2 & -1 \\ -1 & 2\end{pmatrix}$
que tem autovalores $\lambda_2=3$ e $\lambda_3=1$. Para $\lambda_2=3$, o autovetor $w^{(2)}$ pode ser obtido resolvendo
$(B'-3I)w^{(2)}=\begin{pmatrix}0 \\ 0\end{pmatrix}$ => $w^{(2)}=\begin{pmatrix}1 \\ -1\end{pmatrix}$
