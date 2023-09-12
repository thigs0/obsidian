Um conjunto é dito convexo se para qualquer dois pontos do conjunto, é possível construir um segmento de reta, tal que ela permanece dentro do conjunto
$$S\in \mathbb{R}^n; \text{é convexo se  } x,y\in S~~\lambda \in [0,1]\to \lambda x+(1-\lambda)y \in S$$
![[convexo.png|center]]

**Teorema**
Seja $f\in C^1$. Então f é convexa em S se e somente se para todo $x,y\in S$ se verifica
$$f(y)\geq f(x)+\nabla^t f(x)(y-x)$$

**propriedades**
- A intersecção de [[Conjuntos]] convexos é um conjunto convexo