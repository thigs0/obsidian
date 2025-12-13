**Def** Sejam X e Y variáveis aleatórias, a [[Esperança]] condicional de $X_1$, dado $Y=y_0$ é definida como sendo
$$\mathbb{E}[X|Y=y_0]=\mathbb{E}[X|Y=y_0]\begin{cases} \sum\limits_x xP_{X|Y}(x|y_0),~~caso~~discreto\\ \int xf_{X|Y}(x|y_0),~~caso~~contínuo \end{cases}$$
onde $P_{X|Y}(x|y)=P(X=x|Y=y)$

**Resultados**
1) Se X e Y independentes, então $\mathbb{E}[X|Y]=\mathbb{E}[X]$
2) $\mathbb{E}[XY|Y=y]=y\mathbb{E}[X|Y=y]$ 
	**Demonstração**
	$\int xyf_{X|Y}(x|y)dx=y\int xf_{X|Y}(x|y)dx$ 
**Demonstração**:
$\displaystyle \mathbb{E}(\mathbb{E}[X|Y])=\int \mathbb{E}[X|Y=y]f_y(y)dy=\int(\int xf_{x|Y}(x|y)dx)f_y(y)dy=\int\int xf_{x|Y}(x|y)f_y(y)dxdy$
$=\int x(\int f_{X,Y}(x,y)dy)dx=\int xf_x{x}dx=\mathbb{E}(X)$


3) $\mathbb{E}(\mathbb{E}[X|Y]))=\mathbb{E}(X)$


**Exemplo: 1**
$X, Y$ $f_{X,Y}(x,y)=\begin{cases} \frac{1}{y}e^{-\frac{x}{y}}e^{-y},~~x>0~~y>0\\ 0,~~ c.c \end{cases}$
$f_Y(y)=e^{-y},y>0$, Y~exp(1) e $X|(Y=y)$~$exp(1/y)$
1) $\mathbb{E}(XY)=\int_0^\infty \int_0^\infty xy.\frac{1}{y}e^{-\frac{x}{y}}e^{-y}dxxy=\int_0^\infty e^{-y}\left( \int_0^\infty xe^{-\frac{x}{y}}dx \right)dy$ 