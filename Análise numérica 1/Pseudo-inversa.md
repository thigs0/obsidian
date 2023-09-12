- Chamada pseudo-inversa de Moore-Penrose
- Generaliza a inversa de [[Matriz]]es quando são singulares e não quadradas

Seja $\displaystyle A \in \mathbb{R}^{n_xm}$ de [[Posto]] cheio

$\displaystyle \large A^{\dagger} = \begin{cases} (A^{t}A)^{-1}A^{t},\hspace{2cm}Se~n>m\\ \\ A^t(AA^{t)^{-1},}\hspace{2cm}Se~n<m\end{cases}$

---
Outra forma de se definir é usando decomposição [[SVD]]
$$\large A^{\dagger} = V\Sigma^{\dagger}U^t$$
em que $\large \displaystyle \sigma^{\dagger} = \begin{cases} \displaystyle \frac{1}{\sigma_{i}}\hspace{1cm} 1 \leq i \leq p\\ 0 \hspace{1cm}p<i\leq n \end{cases}$ 

- Quando calculamos a pseudo-inversa com os métodos acima, ela fica tão cara quanto a inversa normal




---
**Referências**
A. Ben-Israel and T. N. E. Greville, Generalized inverses: theory and applications,Springer, 2nd edition, (2003)


