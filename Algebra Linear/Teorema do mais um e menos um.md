- Seja S = $\{V_1,...,v_n\} \subset V$ 
A) (Mais um) Se S é [[Linear independente]] e $v \notin ger(S)$, então $S \cup \{v\}$ é LI
B) (Menos um) Se $v_1 \in S$ pode ser expresso como combinação linear dos outros vetores de S, então S\ $\{v_1\}$ = $\{v_2,...v_n\}$ gera o mesmo espaço que S

Prova (A)
	$\sum_{n=1}^\infty \alpha_nv_n + \beta v =0$
	Se $b \neq 0$ -> $\displaystyle V = \frac{-\alpha_1v_1 - \alpha_2v_2-...-\alpha_nv_n}{\beta} \Rightarrow v \in ger()$
	O que é falso -> $\beta =0$, temos estudar $\alpha_1v_1+...\alpha_nv_n=0$ 
	Como S é LI, $\alpha_1 = \alpha_2=...=\alpha_n=\beta=0$
	$S \cup \{V\}$ é LI

Prova (B)
	$V_1 = \alpha_2v_2 + ...+\alpha_nv_n$. Dado $x \in ger(\{v_1,...,v_n\}) \Rightarrow x = \beta_1v_1+\beta_2v_2+...+\beta_nv_n$ 
	= $\beta_1(\alpha_2v_2 +...+\alpha_nv_n)+\beta_2v_2+...+\beta_nv_n$
	= $(\beta_1\alpha_2+\beta_2)v_2+...+(\beta_1\alpha_n+\beta_n)v_n \in ger(v_2,...,v_n)$


**Corolário**
	Seja $S \subset V$ um conjunto finito talque ger(S) = V, então existe subconjunto de S que é base V

**Corolário**
	Seja V de dim finita e $S \subset V$ LI, então S pode ser estendida a uma base
	Prova: Seja ger(S)=V, S é base V. Senão $\exists v \in V$ tq $v \notin ger(S) \Rightarrow S \cup \{V\}$ é LI
	i) o processo para com $S \cup \{V_1,...,v_n\}$ LI e gerando v, uma base 
	ii) O processo não para, mas isso é impossível para dim v < $\infty$

**Corolário**
	V espaço vetorial dim V = n. Se $S \subset \{V\}$ tem n vetores, então S é base v se vale pelo menos uma das duas afirmações abaixo
	A) ger(S) = v
	B) S é LI