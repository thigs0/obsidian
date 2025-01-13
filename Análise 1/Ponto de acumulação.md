Seja $X\subset \mathbb{R}$. Então $a\in X$ é ponto de acumulação se para todo $\epsilon >0$ temos $]X-a,X+\epsilon[\cup (X\{x\})\neq \emptyset$

X' = {$x\in X$:x é de acumulação}

#### Teorema
Seja $X\subset \mathbb{R}$ e $x\in X$. Então, as seguintes afirmações são verdadeiras:
1) $x\in X'$
2) Existe $(X_n)$ [[Cálculo 3/Sequência|Sequência]] de elementos em X tal que $x\to a$ e $x_n\neq x_m,~\forall n,m \in \mathbb{N}$
3) Pelo intervalo contido X possui infinitos elementos de X

1 => 2
Para $\epsilon=1$, existe $x_1\in X$ tal que $0< |x-x_1|<1$
toma $\epsilon = \min \{|x-x_1|,1/2\}$

PROVAR


#### Teorema
Para $X\subset \mathbb{R}$ temos $\bar X=X'\cup X$
**Demonstração:** Sabemos que $X'\subset \bar X$ e $X\subset \bar X$ => $X'\cup X\subset \bar X$ 
Falta ver que $\bar X\subset X'\cup X$

##### Corolário
X é fechado <=> $X'\subset X$ 
=> $X=\bar X=X'\cup X\Rightarrow X'\subset X$

$\Leftarrow$ Supondo $X'\subset X$ logo $X'\cup X=X$
logo X é fechado

##### Corolário
Se todos os pontos de X são isolados então X é enumerável
**Demonstração**: Pelo teorema de [[Densidade]], existe $E\subset X$ enumerável e denso em X seja $x\in X$, então $x\in E$(Pela densidade)
Por hipotese X é isolado. Então $x\notin X'$. Logo $x\notin E'$ Mas, como $x\in \bar E=E\cup E'$
Logo $x\in E$ (Pois $x\notin E'$)
=> $X\subset E\subset X \Rightarrow X=E$
X é enumerável