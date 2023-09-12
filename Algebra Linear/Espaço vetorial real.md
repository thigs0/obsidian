
**Axiomas**
1. Se u e v são objetos em V, então u+v é um objeto em V
2. u+v = v+u
3. u+(v+w) = (u+v)+w
4. Existe um objeto em V, denominado vetor nulo de V, ou vetor zero, tal que 0+u = u+0 =u
5. Dado qualquer u em V, existe algum objeto -u, tal que u+(-u) = (-u)+u = 0
6. Se a for qualquer escalar e u um objeto em V então au é um objeto em V
7. a(u+v) = au + av
8. (a+b)u = au + bu
9. a(bu) = (ab)u
10. 1u = u

**[[Complemento ortogonal]]**
- V espaço vetorial com [[Produto interno]] $W \subset V$ [[Subespaços]]
- um [[Vetor]] V é ortogonal a W, se $\forall w \in W, <v,w>=0$
O conjunto de todos os vetores ortogonais à W, denotamos pot $W^\perp$ 

**Teorema**
- $W^\perp \cap W = \{0\}$
Prova:
	<x+y,w> = <x,w>+<y,w> = 0 -> ambos são 0
	<$\alpha x$,w> = $\alpha$<x,w> = 0$\alpha$ =0
- $(W^\perp)^\perp = W$
Prova:
	$w \in W$ e $w \in W^\perp$ -> <w,w> =0 -> w=0

**Lema**: $A \in \mathbb{R}^{m_xn}$
A) Nulo(A) = (linha A$)^\perp$ 
B) Nulo($A^T$) = (Coluna A$)^\perp$ 
