Sejam (x,y) os pontos da cônica, podemos considerar que eles são as cônicas sobre o eixo, porém rotacionadas. Para isso, aplicamos a [[Matriz de rotação]]
$$\begin{pmatrix}x \\ y\end{pmatrix}=\begin{pmatrix}Cos(\theta)  & -Sin(\theta) \\ Sin(\theta) & Cos(\theta)\end{pmatrix}\begin{pmatrix}x' \\ y'\end{pmatrix}$$
Em que $x'$ e $y'$ são pontos de uma cônica sobre os eixos. Como a matriz é [[Matriz ortogonal]], encontramos rapidamente a inversa e os pontos $x'$ e $y'$.
Sabendo que a equação geral das cônicas é $$Ax^2+Byx+Cy^2+Dx+Ey+F=0$$
podemos aplicar o $x'$ e $y'$ nela e isolar os componentes. Assim cairemos no seguinte sistema
$$\begin{array} 1A' =A\cos^2(\alpha)+B\cos(\alpha)\sin(\alpha)+C\sin^2(\alpha)
\\ B'=B(\cos^2(\alpha)-\sin^2(\alpha))+2(C-A)\sin(\alpha)\cos(\alpha)\\ C'=A\sin^2(\alpha)-B\sin(\alpha)\cos(\alpha)+C\cos^2(\alpha)\\D'=D\cos(\alpha)+E\sin(\alpha)\\E'=-D\sin(\alpha)+E\cos(\alpha)\end{array} \tag{1}$$
Como queremos obter uma cônica com apenas termos de $x^2,~y^2$.
Impomos que $B'=0$ =>
$B(\cos^2(\alpha)-\sin^2(\alpha))=-2(C-A)\sin(\alpha)\cos(\alpha)$ =>
$\displaystyle \frac{\cos^2(\alpha)-\sin^2(\alpha)}{\sin(\alpha)\cos(\alpha)}=\frac{-2(C-A)}{B}$ => $\displaystyle \frac{-2\sin(\alpha)\cos(\alpha)}{\cos^2(\alpha)-\sin^2(\alpha)}=\frac{B}{C-A}$. Pode parecer abstração. mas essa fórmula envolvendo seno e cosseno, é igual á $Tg(2\alpha)$ Assim
$$Tg(2\alpha)=\frac{B}{C-A}$$

### Exercícios.

Rotacionamos a cônica dada por $$7x^2+48xy-7y^2+25=0$$
![[Exercicio_conica1.png|center|300]]
- Encontramos a tangente
$\displaystyle Tg(2\alpha) = \frac{B}{C-A}=\frac{48}{7-(-7)}=\frac{24}{7}$
Sabemos que a $\displaystyle Tg(2\alpha)= \frac{\sin(2\alpha)}{\cos(2\alpha)}=\frac{\text{Cateto oposto}}{\text{Cateto adjacente}}$
E sabemos que $\displaystyle \cos(2\alpha)=\frac{\text{Cateto Adjacente}}{Hiponusa}$ De cima tiramos que Cateto adjacente=7.
E Hipotenusa=$\sqrt{\text{(cateto oposto)}^2+\text{(Cateto adjacente)}^2}=\sqrt{24^2+7^2}=25$
Assim, $Cos(2\alpha)=\frac{7}{25}$
Usando as relações trigonométricas abaixo, podemos encontrar $\cos(\alpha)$
$$\displaystyle \begin{cases}\cos(\alpha)=\displaystyle\sqrt{\frac{1+\cos(2\alpha)}{2}}\\ \sin(\alpha)= \displaystyle\sqrt{\frac{1+\cos(2\alpha)}{2}}\end{cases}$$
Encontramos que $\cos(\alpha)=4/5$ e $\sin(\alpha)=3/5$
Com os termos da rotação, aplicamos a equação 1.
$A'=7\frac{16}{25}+48\frac{6}{13}-7\frac{9}{25}=25$
$B'=0$
$C'=-25$
$D'=E'=0$
$F'=25$
Agora, plotando nossa nova cônica $25x^2-25y^2+25=0$ => $y^2-x^2=1$
![[Exercicio_conica2.png|center|300]]
