$\huge\textbf{Teorema~fundamental~da~integral~de~linha}$ --> Seja C uma curva suave dada pela função vetorial $r(t)\leq t\leq b$. Seja f uma função diferenciável de duas ou três variáveis cujo vetor gradiente $\nabla f$ é contínuo em c. Então:$$\int_C \nabla f \cdot dr = f(r(b))-f(r(b))$$ 
	Assim podemos avaliar a integral de linha de um [[campo conservativo]] sabendo apenas os pontos finais e iniciais


$\huge\textbf{teorema}$ -->  $\displaystyle \int_C F\cdot dr$ é independente do caminho em D se e somente se $\displaystyle \int_C F\cdot dr =0$ para todo caminho fechado C em D

$\huge\textbf{Teorema}$ Suponha que F seja um campo vetorial contínuo em uma região aberta conexa por caminhos D. Se $\int_C F\cdot dr$ for independente do caminho em D, então F é um campo vetorial conservativo em D, ou seja, existe uma função f tal que $\nabla f = F$ 
	é o retorno para o teorema acima


$\huge \textbf{Teorema}$ --> Se $\vec F (x,y)= P(x,y)\hat i + Q(x,y)\hat j$ é um campo vetorial conservativo, onde P e Q têm derivadas parciais de primeira ordem contínuas em um domínio D, então em todos os pontos de D temos $$\frac{\partial P}{\partial y}= \frac{\partial Q}{\partial x}$$

**[[Trabalho]]**
O trabalho usa a integral de linha em sua definição $W = \vec F \cdot \vec {AB}$
Seja $\vec T (x,y,z)$ o vetor tangente a C em (x,y,z), $||\vec T||=1$
$$\int_C \vec F \cdot \vec {dr}= \int_a^b \vec F(r(t))\cdot \vec r(t)dt = \int_C \vec F \cdot \vec T ds$$
**Exercício**
Calcule $\int_C (2+x^2y)ds$
C é uma semicircunferencial positiva de raio 1
$\int_0^\pi (2+cos^2(t)sen(t))\sqrt{cos^2(t)+sen^2(t)}dt$
