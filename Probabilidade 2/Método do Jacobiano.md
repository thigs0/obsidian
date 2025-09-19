- Usa a [[Jacobiana]]
Seja $X$ um [[Vetor]] aleatório com densidade conjunta $f_X$ e queremos estudar $Y=g(X)$.
e uma [[bijeção]] com $h=g^{-1}$ existindo suas [[Derivada]]s 

$$f_Y(y) = |J_h(y)|.f_X(h(y))=\frac{1}{|J_g(h(y|}f_X(h(y))$$
**Exemplo**
$f_X(x_1,x_2)=\begin{cases} 4x_1x_2,~~x_1,x_2\in [0,1]\\ 0,~~c.c \end{cases}$       e o vetor $Y$ dado por $\displaystyle Y_1=\frac{X_1}{X_2}$ e $Y_2=X_1X_2$ com $y=g(x)=x_1/x_2,x_1x_2$ 
$\displaystyle \frac{\partial y}{\partial x}=\displaystyle \begin{pmatrix} \frac{1}{x_2} & \frac{-x_1}{x_2^2}\\ x_2 & x_1 \end{pmatrix}$ e $J_g(x)=\frac{1x_1}{x_2}$ obtendo $x$ em [[função]] de $y$, temos que $x_1=\sqrt{y_1y_2},~~x_2=\displaystyle \sqrt{\frac{y_2}{y_1}}$ 
$$G=\{ (y_1,y_2):0<y_2<y_1,0<y_2<\frac{1}{y_1} \}$$
com $J_g(h(y))=\displaystyle \frac{2\sqrt{y_1y_2}}{\sqrt{\frac{y_2}{y_1}}}=2y_1$ e $f_X(h(y))=4\sqrt{y_1y_2}\sqrt{\frac{y_2}{y_1}}=4y_2$ 

$$f_Y(y)=\frac{1}{|J_g(x|}f_X(h(y))=\begin{cases} 2y_2/y_1,~~0<y_2<1\\ 0,~~c.c \end{cases}$$
