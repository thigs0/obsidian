- Aproximamos o [[Método de Newton para sistemas]], de modo que fique mais barato, mas ainda tenhamos convergência próxima da quadrada.

- Substituem a [[Jacobiana]] por uma aproximação

#### Método de Broyden
Aproximamos a Jacobiana com a anterior
Aproximando pela Secante:
$$J(x^{(1)})(x^{(1)}-x^{(0)}) \approx F(x^{(1)})-F(x^{(0)})$$
- No método substituímos $J(x^{(1)})$ por uma [[Matriz]] $A_1$ com a propriedade:
$$A_1(x^{(1)}-x^{(0)})=F(x^{(1)})-F(x^{(0)})$$
Observe que qualquer vetor de $\mathbb{R}^n$ pode ser escrito como a soma de um múltiplo de $x^{(1)}-x^{(0)}$ e um múltiplo de um vetor no complemento ortogonal de $x^{(1)}-x^{(0)}$. Para definir $A_1$ como única, necessitamos especificar como ela age no [[Complemento ortogonal]] de $x^{(1)}-x^{(0)}$. Vamos pedir somente que:
$$A_1z=J(x^{(0)})z, ~~~\text{Qualquer que seja}$$
Temos$$A_1=J(x^{(0)})+\frac{[Fx^{(1)}-F(x^{(0)})-J(x^{(0)})(x^{(1)}-x^{(0)})]}{\|x^{(1)}-x^{(0)}\|_2^2}(x^{(1)}-x^{(0)})^t$$
- Que atende as equações que citamos acima
- O método é repetido para obter $x^{(3)}$, utilizando $A_1$ no lugar de $A_0=J(x^{(0)})$ e $x^{(2)}, x^{(1)}$ no lugar de $x^{(1)}$ e $x^{(0)}$, respectivamente.

$s_k=x^{k+1}-x^{k}$ e $y^k=F(x^{k+1})-F(x^k)$ 
$\displaystyle \large J_{k+1}=J_{k}+\frac{y^k-J_ks_k}{s_k^ts_k}s_k^t$ 

----
**Exemplo**
$$F(x)=\begin{pmatrix}3x_1-\cos(x_2x_3)-1/2\\x_1^2-81(x_2+0.2)^2+\sin(x_3)+1.06 \\ e^{-x_2x_3}+20x_3+\frac{10\pi+3}{3}\end{pmatrix}$$
Resolva o sistema acima usando o método quase-newton com $x^{(0)}=\begin{pmatrix}0.1 \\ 0.1 \\ -0.1\end{pmatrix}$ 
$J(x)=\begin{pmatrix}3 & x_3\sin(x_2x_3) & x_2\sin(x_2x_3) \\ 2x_1 & -162(x_2+0.1) & \cos(x_3) \\ -x_2e^{-x_1x_2} & -x_1e^{-x_1x_2} & 20\end{pmatrix}$
De inicio usamos a jacobiana.
$J(x^{(0)})=\begin{pmatrix}3 & -0,000017453 & -0,00001745 \\ 0.2 & -32,4 & 0,999998477 \\ 0,002718282 &0,002718282 & 20 \end{pmatrix}$ 
Encontramos o $x_1$
$J(x^{(0)})d=-F(x^{(0)})$ 