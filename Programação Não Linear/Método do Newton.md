$f:\mathbb{R}\to \mathbb{R}$; $f(x)=x^tAx+b^tx+c$; $A\in \mathbb{R}^{n\times n}$;$b\in \mathbb{R}^n$, $c\in \mathbb{R}$ e $A$ é uma [[Matriz definida positiva]]
Seja $x^*$ um ponto [[Minimizador]] da função e $x$ o ponto que iniciamos
como mostra a imagem abaixo
![[curva.png|center|300]]
$$\begin{align}d=x^*-x\\ d=-A^{-1}b-x\\ d=-A^{-1}[b-Ax]\\ d=A^{-1}\nabla f(x)\\ d=-[\nabla^2 f(x)]^{-1}\nabla f(x)\Leftrightarrow \boxed{\nabla^2f(x)d=-\nabla f(x)}\end{align} $$
Assim, temos uma outra forma de resolver uma cônica. Aproximamos a nossa função por [[Polinômio de Taylor]]
$$f(x)\approx q(x)=f(x^k)+\nabla f(x^k)^t(x-x^k)+\frac{1}{2}(x-x^k)^t\nabla^2f(x^k)(x-x^k)$$
- Quanto mais próximo do mais rápido converge, visto que converge diretamente para o mínimo local da cônica

**Teorema** 
Seja $x^*\in \mathbb{R}^n$ um minimizador local de $f$ satisfazendo as condições suficientes de segunda ordem. Então, existe $\epsilon >0$ tal que se $\|x^0 -x^*\|<\epsilon$, a [[Sequência]] $x^{k+1}=x^k-[\nabla^2 f(x^k)]^{-1}\nabla f(x^{k})$ está bem definida para todo $\mathbb{R}\in \mathbb{N}$, converge para $x^*$ e existe $c>0$ tal que $\|x^{k+1}-x^{*}\|\leq c\|x^k -x^*\|^2$, para todo $k\in \mathbb{N}$ 

##### Algoritmo
Dados $x^0\in \mathbb{R}^n$, $\alpha \in (0,1),~\beta >0~,\gamma \in (0,1],k=0$ 
**Enquanto** $\|\nabla f(x^k)\|\neq 0$ 
	**Tente**
		Resolva $\nabla^2 f(x^k)d^k=-\nabla f(x^k)$
	**Se deu errado**
		$d^k=-\nabla f(x^k)$
	**Se** $\nabla f(x^k)d^k >-\gamma \|\nabla f(x^k)\|.\|d^k\|$
		$d^k=-\nabla f(x^k)$ 
	**Se** $\|d^k\|< \beta \|\nabla f(x^k)\|$
		$d^k\leftarrow \frac{d^k}{\|d^k\|}\|\nabla f(x^k)\|\beta$
	$t_k=1$ 
	**Enquanto** $f(x^k+t_kd^k)>f(x^k)+\alpha t_k \nabla f(x^k)^td^k$
		$t_k\leftarrow t_k/2$ 

Caso a função seja singular, modificamos a [[matriz]] para que ela não seja singular
$\nabla^2 f(x) \leftarrow \nabla^2 f(x^k)+\mu I$
e esta função quando $\mu$ aumenta, tende a termos um múltiplo do [[Gradiente]]. Assim, escolhemos um $\mu_0$ de modo que se não passar nas condições, aumentamos o valor

---
Assim, temos como condição geral
$$\boxed{B_kd^k=-\nabla f(x^k)}$$
em que $b_k$ é [[Matriz definida positiva]] e cada escolha de $B_k$ define um método
