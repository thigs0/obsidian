
##### Definição
O produto interno é uma função <.,.> $V.V$ ->R tal que
 1. $\forall~ x \in V, ~<x,x> ~\geq0,~ <x,x> =0 ~~se~ x=0$
 2. $\forall x,w\in V~~ <x,w>=<w,x>$
 3. $\forall x \in V, ~ \alpha \in \Re ~~~ <\alpha x,w>=\alpha <x,w>$
 4. $\forall x,w,y ~~~~<x+w,y>=<x,y>+<w,y>$ 

Definição de produto interno é qualquer objeto que tenha as propriedades 

**Para o caso contínuo** e limitado entre [0, 1]
	é definido como 
	$\displaystyle <f, g>=\int_0^1 f(x) {g(x)}dx$ 

**Propriedades**
1. <0,x> = 0
2. <x, $\alpha x$> = $\alpha$<x,y>
3. <x, y+z> = <x,y>+ <x,z>
4. $|x+y|^2 = ||x||^2 + 2<x,y> + ||y||^2$


#### [[Desigualdade de Cauchy-Schwarz]]
- -> Se $\vec u$ e $\vec v$ forem [[Vetor]]es num espaço com produto interno real V, então$$\large |<\vec u,\vec v>| \leq ||\vec u||||\vec v||$$
	- Prova:
		a= <u,u>;   b=2<u,v> ;   c=<v,v> e $t \in \mathbb{R}$
		$0\leq~ <tu+v,~tu+v> = <u,u>t^2+2<u,v>t+<v,v> = at^2+bt+c$
		Usando báskara:
		$4<u,v>^2-4<u,u><v,v>~\leq 0 ~~~~\Rightarrow ~~~~~ <u,v>^2 \leq <u,u><v,v>$

#### Definição
Dizemos que dois vetores u e v de um espaço com produto interno são ortogonais se _<u,v>_ = 0  

#### Definição: Complemento ortogonal
Se W for um subespaço de um espaço com produto interno C, então o conjunto de todos os vetores em V que são ortogonais a cada vetor em W é denominado [[Complemento ortogonal]] de E e denotado por $W^\perp$

**[[Projeção]]**
A projeção de um vetor $\vec B$ em um vetor $\vec A$ é dado pelo produto escalar entre os dois vetores dividindo pela norma de $\vec B$ 
$$\vec {Proj_{B,A}} = \left ( \frac{\vec B . \vec A}{||\vec A||^2}\right)\vec A$$
