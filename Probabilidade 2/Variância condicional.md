A [[Variância]] condicional de X, dada pelo $Y=y$ é definida por $$var[X|Y=y]=\mathbb{E}[X^2|Y=y]-(\mathbb{E}[X|Y=y])^2$$
**Propriedades**
1) $Var(X)=\mathbb{E}[Var[X|Y]]+Var(\mathbb{E}[X|Y])$ 
***Demonstração***
$var(\underbrace{\mathbb{E}[X|Y]}_{E})=\mathbb{E}((\mathbb{E}[X|Y])^2)-(\mathbb{E}(\mathbb{E}[X|Y]))^2=\mathbb{E}((\mathbb{E}[X|Y])^2)-(\mathbb{E}(x))^2$ 
2) $\mathbb{E}(Var[X|Y])=\mathbb{E}(\mathbb{E}[X^2|Y]-(\mathbb{E}[X|Y])^2)=\mathbb{E}(X^2)-\mathbb{E}((\mathbb{E}[X|Y])^2)$
Usando (1) + (2) => $\mathbb{E}[X^2]-(\mathbb{E}(X))^2=Var(X)$

### Exemplos
1) $f_{X,Y}(x,y)=\begin{cases} \frac{1}{y}e^{-y},0<x<y\\ 0,~~c.c \end{cases}$
$\mathbb{E}[X^k|Y=y]$
$f_Y(y)=\int_0^y \frac{1}{y}e^{-y}dx=e^{-y},y>0$
$f_{X|Y}(x|y)=\frac{f_{X,Y}(x,y)}{f_Y(y)}=\frac{\frac{1}{y}e^{-y}}{e^{-y}},~~0<x<y$
$=\frac{1}{y}$ então $X|Y=y$~$U(0,y)$
$Var(X)=\mathbb{E}(Var[X|Y])+Var(\mathbb{E}[X|Y]))=\mathbb{E}\left(\frac{Y^2}{12}\right)+Var\left( \frac{Y}{2} \right)=\frac{1}{12}\mathbb{E}(Y^2)+\frac{1}{4}Var(Y)$
