Transformação de Householder ou Refletores

### Caso n=2
Seja r uma reta de $\mathbb{R}^2$ que passa pela origem. Seja $v\neq 0,~v\in r$.Tome $u \in \mathbb{R}^2$ tal que $u \neq 0$, $u \perp v$.
$\{u,v\}$ é base do $\mathbb{R}^2$

---

Vamos supor sem perda de generalidade, que $\|u\|_2=1$. Considere a [[Matriz]] $P=uu^t~~\in \mathbb{R}^{2_x2}$ 
$\begin{cases} Pu = u\underbrace{u^tu}_{I} = u\|u\| = u\\ Pv = u\underbrace{u^tv}_{perpendiculares}=u.o=0\end{cases}$
- Será que usamos P e a identidade não conseguimos a reflexão que satisfaz
(I) Tomemos $Q = I-\gamma P$ 
	$Qu = (I-\gamma P)u = (I-\gamma uu^t)u =u- \gamma u = -u$
	$Qv=(I-\gamma P)v = v-\gamma uu^tv = v$
	Dos dois acima tiramos $\gamma =2$

Portanto, se tomarmos $Q = I-2uu^t$, onde u é um vetor unitário ortogonal a reta r, temos:

---

$$\begin{cases} Qu=-u\\ Qv=v\end{cases}$$
Ou seja, temos que Q é uma transformação do tipo reflexão.

---

**Teorema**
	Seja $u \in \mathbb{R}^n$, tal que $\|u\|_2=1$, defina $P \in \mathbb{R}^{n_xn}$ por P=$uu^t$. Então
	a) $Pu=u$
	b) $Pv  =0$
	c) $P^2 = P$
	d) $P^t = P$

**Teorema**
	Seja $u \in \mathbb{R}^n$ tal que $\|u\|=1$ e defina $0 \in \mathbb{R}^{n_xn}$ por $Q=I-2uu^t=I-2P$. Então
	a) $Qu = -u$
	b) $Qv = v,~~se~<u,v>=0$
	c) $Q=Q^t$
	d) $Q^t=Q^{-1}$
	e) $Q^{-1}=Q$

1) A parte (a) do teorema anterior implica que $$Qw = -w$$
2) As matrizes do tipo $Q=I-2uu^t$, $\|u\|=1$, são conhecidas por refletores ou transformação de Householder

**Teorema**
Seja u um vetor não nulo em $\mathbb{R}^n$ e defina $\displaystyle \gamma = \frac{2}{\|u\|_2}$ e $Q=I-\gamma uu^t$. Então Q é um refletor