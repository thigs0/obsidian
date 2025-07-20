- é obtido determinando a maior das [[Relações fuzzy]], que satisfazem uma versãi mais fraca

De maneira geral $$\overset{\vee}{\mathcal{R}}(x,y)=\displaystyle\vee^k_{i=1} (A_i(x)\Delta B_i(y))$$

#### Exemplo
Considere a base de regra

| Se          |       Então      |
| ----------- | ----------- |
| x é pequeno | y é pequeno |
| x é médio   | y é médio   |
| x é grande  | y é grande            |
- No [[método de inferência de Mandani]], definimos a relação
$\overset{\vee}{\mathcal{R}}(x,y)=\vee_{i=1}^3 A_i(x)\wedge B_i(y), ~~\forall (x,y)\in X\times Y$


**Definição de** [[Resíduo de uma conjunção fuzzy]]
Dada uma conjunção fuzzy $\mathcal{C}:[0,1]\times [0,1]\to [0,1]$, o operador $\mathcal{I}_\mathcal{C}:[0,1]\times [0,1]\to [0,1]$ dado por $$\mathcal{I}_\mathcal{C}(a,b)=\vee \{z\in [0,1]:\mathcal{C}(a,z)\leq b \},~~\forall a,b\in [0,1]$$**Teorema**
- Seja $\mathcal{C}:[0,1]\times [0,1]\to [0,1]$ uma conjunção fuzzy tal que $\mathcal{C}(1,z)=0$ se e somente se z=0. Nesse caso o resíduo da conjunção fuzzy é uma implicação fuzzy, denotada por $\mathcal{I}_\mathcal{C}$ chamada implicação residual ou R-implicação associada a conjunção fuzzy $\mathcal{C}$
- ***Corolário***
	- O resíduo de uma [[t-norm]] é uma implicação residual $\mathcal{I}_\Delta$, também denotada por $\to_\Delta$  

**Método de composicional de inferência**
No caso da regra, definimos $$\psi^\circ_{\mathcal{R}}(A)=A\cdot \mathcal{R}$$
**teorema**
Seja $([0,1],\vee,\wedge,\Delta,\to)$ um reticulado completo residuado. Considere uma base de regras
$$\textbf{Se}~\text{x é } A_j  \text{ Então y é } B_i,~~\forall i=1,2,...k$$
Se existe uma relação fuzzy $\mathcal{R}\in \mathcal{F}(X\times Y)$ tal que a regra composicional de inferência é consistente com a base de regras fuzzy, então o método de inferência conjuntivo é também consistente com a base de regras fuzzy, ou seja
$$\psi^\circ_\mathcal{R}(A_i)=A_j\circ \mathcal{R}=B_i,~~\forall i=1,2,...,k$$









