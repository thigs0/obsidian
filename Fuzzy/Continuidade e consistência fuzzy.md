- Chamado de [[Teorema da equivalência de Perfilieva-Lehmke]]
Seja $\mathcal{L}=([0,1],\vee,\wedge,\Delta,\to)$ um [[reticulado residuado]] e $\sigma_\mathcal{L}$ a medida de similaridade natural de $\mathcal{L}$. Dada uma [[Base de regras]] de um [[conjunto fuzzy]]
$$\text{Se x é} ~~A_i~~\text{Então y é}~~B_i,~~\forall i,....,k$$
e uma das [[Relações fuzzy]] $\mathcal{R}\in\mathcal{F}(X\times Y)$, a [[função]] $\psi_\mathcal{R}^\circ:\mathcal{F}(X)\to \mathcal{F}(Y)$ dada pela RCI, isto é$$\psi_\mathcal{R}^\circ(A)=A\circ \mathcal{R}$$
é contínua se e somente se é consistente com a base de regras

**Demonstração**
Sabemos que continuidade implica consistência. vamos mostrar que se $\psi_\mathcal{R}^\circ$ é consistênte, então é contínuo. Com efeito.
$$\sigma_Y(\psi_\mathcal{R}^\circ(A),B_i)=\sigma_Y(\psi_\mathcal{R}^\circ(A),\psi_\mathcal{R}^\circ(A_i))=\wedge_{y\in Y}(\psi_\mathcal{R}^\circ(A)(y)\leftrightarrow \psi_\mathcal{R}^\circ(A_i)(y))$$
Mas para qualquer $y\in Y$, tem-se
$\psi_\mathcal{R}^\circ(A)(y)\leftrightarrow \psi_\mathcal{R}^\circ(A_i)(y)$
$=\left[ \vee_{x\in X} A(x)\Delta \mathcal{R}(x,y)\right]\leftrightarrow \left[ \vee_{x\in X}A_i(x)\Delta \mathcal{R}(x,y) \right]\geq \wedge_{x\in X} [A(x)\Delta \mathcal{R}(x,y)]\leftrightarrow [A_i(x)\Delta \mathcal{R}(x,y)]$
$\geq \wedge_{x\in X}[A(x)\leftrightarrow A_i(x)]\Delta [\mathcal{R}(x,y)\leftrightarrow \mathcal{R}(x,y)]=\sigma_X(A,A_i)$
Logo $\sigma_Y(\psi_\mathcal{R}^\circ(A), B_i)\geq \sigma_X(A,A_i)$ e portanto, $\psi_{\mathcal{R}}^\circ$ é contínuo
