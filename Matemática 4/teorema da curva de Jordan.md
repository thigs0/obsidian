Seja $\gamma :S^1$->$C$ uma curva de Jordan. Então $C-\gamma (S^1)$ possui duas componentes conexas, uma limitada e a outra ilimitada. Além disto, o bordo de cada uma destas componentes é a curva $\gamma(S^1)$ 
- A componente limitada de $C-\gamma(S^1)$ será chamada de componente ou região interior e a ilimitada se exterior
![[jordan_curve.png|center|400]]
**Demonstração**:
	Seja $\gamma :S^{1}\rightarrow C$ uma curva de classe $C^2$, isto é, ela é [[Contínua]] no plano
	Podemos parametrizar a curva de forma $\alpha (\theta) = \gamma(e^{i\theta})$. Então o vetor tangente a $\gamma$ no ponto $\gamma(e^{i\theta})$ é $\frac{d}{d\theta}\alpha(\theta) \neq 0$.
	Seja f uma função de $f:C^{*}\rightarrow C$ definida como $f(z)=f(re^{i\theta})=\alpha(\theta)+iLn(r)\alpha'(\theta)$. Observe que,$f(e^{i\theta})=\gamma(e^{i\theta})$ e se R é fixo. E definimos	$$A(\epsilon)=\{z \in C^{*}; 1-\epsilon<|z|<1+\epsilon\},~~onde~~\epsilon<1$$	
	**Lema** ([[Vizinhança tubular]])
		Existe $\epsilon>0$ tal que $f(A(\epsilon))$ é um aberto e além disto $f|A(\epsilon):A(\epsilon)\rightarrow f(A(\epsilon))$ é um [[Difeomorfismo]] de classe $C^1$ 
		**Demonstração**
	Imediatamente do Lema acima temos que $C-\gamma(S^1)$ possui no máximo duas componentes conexas.
	Em especial, mostraremos que existem duas componentes conexas.
	