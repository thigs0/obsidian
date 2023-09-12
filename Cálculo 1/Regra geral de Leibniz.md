- generaliza a regra do produto para [[Derivada]]s 
- A prova segue com [[Complementos de matemática/Indução]]

A regra afirma seja f e g [[Funções]] deriváveis até n, então a derivada enésima do produto entre ambas é dado por:
$$(f.g)^{(n)} = \sum_{k=0}^{n} \begin{pmatrix}n \\k\end{pmatrix} f^{(n)}g^{(n-k)} \tag{1}$$

**Demonstração:**
	Testamos para n=0, que pode definição resulta que $h(x)^{(0)} = h(x)$
	=>
	$(f.g)^{(0)} = f.g$
	$\displaystyle \sum_{k=0}^{n} \begin{pmatrix}n \\ k\end{pmatrix}f^{(n)}g^{(n-k)} =\begin{pmatrix}0 \\ 0\end{pmatrix}f^{(0)}g^{(0)} = f.g$ 
	Então a fórmula é válida para n=0.
	Supondo que a fórmula seja válida para um certo n, vou mostrar que também é válida para n+1.
	