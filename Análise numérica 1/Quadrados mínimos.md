- Queremos ajustar [[Funções]] para uma região com dados discretos
	- Dado um conjunto de pares $\Omega \{(t_i, y_i)| i=1,....,m\}$ e um conjunto de funções $\{\phi_1, \phi_2, \phi_3,..,\phi_n\}$, queremos encontrar a função $\phi (t) = \sum_{j=1}^n C_j\phi_j (t)$, que satisfaça
**Exemplo**
![[teste.png]]


$$\min_{c \in \mathbb{R}^n} \sum_{i=1}^m (\phi (t_i)-y_i)^2$$
$\begin{bmatrix} C_1\phi(t_1) + C_2\phi_2(t_1)+...+C_n\phi_n(t_1)\\ C_1\phi_1+C_2\phi_2(t_2)+...+C_n\phi_n(t_2)\\......\\ C_1\phi_1(t_n)+C_2\phi_2(t_n)+...+C_n\phi_n(t_n)\end{bmatrix}= \begin{bmatrix} \phi_1(t_1) & \phi_2(t_1)&...&\phi_n(t_1)\\ \phi_1(t_2) & \phi_2(t_2)&...&\phi_n(t_2)\\ ...\\ \phi_1(t_n) & \phi_2(t_n)&...&\phi_n(t_n) \end{bmatrix}\begin{bmatrix}C_1 \\ C_2\\ ...\\ C_n\end{bmatrix}$

Queremos $\displaystyle \large \min_{C \in \mathbb{R}^n} \| \Phi C - y \|^2$
$\|\Phi C - y\|^2 =(\Phi C -y)^t(\Phi C -y)=(C^t\Phi^t- y^t)(\Phi C -y)=C^t\Phi^T\Phi C- C^t\Phi^ty - y^t\Phi yC+y^ty= C^t\Phi^t\Phi C -2C^t\Phi^ty + y^ty$
Para minimizar a função, veremos o [[Gradiente]] 
$\nabla (\| \Phi C -y\|^2)= 0 \Rightarrow 2\Phi^t \Phi C - 2\Phi^t y=0 \Rightarrow \Phi^t\Phi C = \Phi^t y$
- O sistema acima é chamado [[Sistema Normal]] 


**Avaliar uma operação com [[Matriz ortogonal]]**
	Seja $Q \in \mathbb{R}^{mxn}$ uma matriz ortogonal
	$Q^tAx = Q^tb$ e seja $r$ o resíduo deste sistema transformado, então
	=> $\|s\| = \|Q^t r\|= \|r\|$
	Logo, Q sendo ortogonal implica $\|s\|_2 =\|r\|_2$
	ou seja, o resíduo (s) do sistema transformado, tem a mesma norma do resíduo (r) do sistema original.
	
**Teorema**
Sejam $A \in \mathbb{R}^{mxn}$, m>n. Então existe $Q \in \mathbb{R}^{mxn}$ e $R \in R^{mxn}$, tal que Q é ortogonal e $R= \begin{bmatrix} \hat R \theta \end{bmatrix}$, onde $\hat R \in \mathbb{R}^{nxn}$ e triangular superior e A=QR

dem: 
Seja $\large \bar A = [A | Ã] \in \mathbb{R}^{mxm}$, onde $\large Ã\in \mathbb{R}^{mx(m-n)}$ é escolhida arbitrariamente. Então, existem $\large Q, \bar R \in \mathbb{R}^{mxm}$ tal que Q é ortogonal, $\bar R$ é triangular superior e $\bar A = Q \bar R$.
Agora, particiono $\bar R = [R \\| \~R]$, ONDE $r \in mathbb{R}^{mxn}$ temos 
$\bar A = Q \bar R$ => $[A|Ã] = Q[R|tio(R)] = [QR|Q~tio(R)]$ 

Como $\bar R$ é uma matriz triangular superior e $\bar R= [R|tio(R)]$. Então R tem que ter a forma
$R = \begin{bmatrix} \hat R\\ \theta\end{bmatrix}$; $\hat R \in \mathbb{R}^{nxn}$ é uma matriz triangular superior.

**Teorema**
Seja $A \in \mathbb{R}^{mxn}$ e $b\in \mathbb{R}^{m}$, m>n e sopunhamos que A tem [[Posto]] completo. Então o problema de quadrados mínimos para o [[Sistema linear]] tem uma única solução a qual pode ser obtida resolvendo $\hat R x = \hat c$, onde $\hat c \in \mathbb{R}^n$, $Q^Tb= \begin{bmatrix} \hat c\\d\end{bmatrix}$, Q e $\hat R$ são como os teoremas anteriores A = QR, Q é ortogonal $R = \begin{bmatrix} \hat R\\ \theta\end{bmatrix}$ e $\hat R \in \mathbb{R}^{nxn}$

**Exemplo**
Com [[Decomposição QR]] resolva o problema de quadrados mínimos:
$\begin{bmatrix} 3&-2\\0&3\\4&4\end{bmatrix} \begin{bmatrix}x_1\\x_2 \end{bmatrix}= \begin{bmatrix} 1\\2\\4\end{bmatrix}$

=> $x= \begin{bmatrix} 3\\0\\4\end{bmatrix}$, y=$\begin{bmatrix} 5\\0\\0\end{bmatrix}$, u=x+y= $\begin{bmatrix} 8\\0\\4\end{bmatrix}$ $\|u\| = \sqrt{80}$ 
$Q_1 = I-\frac{2}{80}uu^t = I-\frac{1}{40}\begin{bmatrix} 64&0&32\\0&0&0\\32&0&16\end{bmatrix}$ = $\begin{bmatrix} -0.6&0&-0.8\\0&1&0\\-0.8&0&0.6\end{bmatrix}$ 
$Q_1A = \begin{bmatrix} -5&-2\\0&3\\0&4\end{bmatrix}$


=>
x $= \begin{bmatrix}3\\4 \end{bmatrix}$, y = $\begin{bmatrix}5\\0 \end{bmatrix}$, u = $\begin{bmatrix} 8\\4\end{bmatrix}$, $\|u\|=\sqrt{80}$
$Q_2 = I-\frac{2}{80}uu^t= I-\frac{1}{40}\begin{bmatrix}64&32\\32&16 \end{bmatrix}$

$= \begin{bmatrix} -0.6&-0.8\\-0.8&0.6\end{bmatrix}$


$Q_2.Q_1.A= \begin{bmatrix}-5&-2\\0&-5\\0&0 \end{bmatrix}$
$Q_2Q_1.B= \begin{bmatrix}-3.8\\-2.48\\-0.64 \end{bmatrix}$
Resolvemos o sistema
$\begin{bmatrix} -5&-2\\0&-5\end{bmatrix}x=\begin{bmatrix} -3.8\\-2.48\end{bmatrix}$

