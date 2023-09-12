Considere uma partição básica $\textbf{A=[B~N]}$ e a seguinte solução obtida ao se fixar as n-m variáveis de $\textbf{X}_n$ em zero, isto é
$$\begin{cases}\hat X_B =B^{-1}b\\ \hat X_N=0\end{cases}$$

o $\hat X_B$ obtido é chamado de solução básica
Caso:
- $\hat X_B=B^{-1}b\geq 0$ => temos uma solução básica factível 
- $\hat X_B=B^{-1}b>0$ => Solução básica factível não-degenerada
- Caso algum elemento seja menor que 0, temos uma solução não factível

### Como determinar uma solução básica inicial factível
- Em alguns casos, isso é direto. Por exemplo, considere o caso em que o problema envolve restrições da forma $\mathbf{Ax\leq B}$, onde $b\geq 0$ 
Neste caso inserimos variáveis de folga não negativas e o reescrevemos as restrições como $\mathbf{A}x+\mathbf{s}=\mathbf{b}$ 

*Introduzimos novas variáveis*
Criamos variáveis para obtermos a [[Matriz]] identidade
$$\mathbf{B}x+\mathbf y=\mathbf{b};x\geq0,y\geq 0$$
*Exemplo*
$$\min f(x)=-x_1+2x_2$$
$s.a: \begin{align}x_1+x_2\geq2\\ -x_1+x_2\geq 1 \\x_1\geq 0,x_2\geq 0\end{align}$

Deixamos na forma padrão ->
$A=\begin{pmatrix}1 & 1 & -1 & 0 & 1 & 0 \\-1 & 1 & 0 & -1 & 0 & 1 \end{pmatrix}$ $x=\begin{pmatrix}x_1 \\ x_2 \\ x_3 \\ x_4 \\ y_1 \\ y_2\end{pmatrix}$  $b=\begin{pmatrix}2 \\ 1\end{pmatrix}$
tal que $x\geq 0$ 
Agora temos o problema auxiliar
$f(x,y) = y_1+y_2$
$s.a:Ax=b$ 