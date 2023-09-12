- No equilibrio a temperatura se iguala
- 273K é o ponto triplo da água


+W -> Trabalho realizado pelo sistema
-w -> Trabalho realizado sobre o sistema
  $\Delta E_{int} = Q_{rec}- W_{\text{Pelo sistema}}$

[[Capacidade calorífica]] -> $\displaystyle C = \frac{Q}{\Delta t}$
[[Calor específico]] -> $\displaystyle C = \frac{Q}{m \Delta t}~~ou~~ C_{mol} = \frac{Q}{mol.\Delta t}$

[[Trabalho de um gás]]
O [[Trabalho]] feito por um gás é dado por
$\displaystyle W = \int dw = \int_{v_i}^{v_f} pdv$

[[Primeira lei da termodinâmica]]
	$\Delta E_{int} = E_{int,f} -E_{int,i}= Q-W$
	Q -> Energia trocada por calor
	W -> Trabalho negativo realizado pelo sistema, trabalho positivo sobre o sistema


*Processos*
	Adiabáticos -> Q=0, $\Delta E_{int} = -W$
	Volume constante -> W=0, $\Delta E_{int} = Q$
	Cíclicos -> $\Delta E_{int} =0$, Q = W
	Expansão livre -> Q=W= $\Delta E_{int}=0$


**[[Livre caminho médio]]**
	$\displaystyle \lambda = \frac{\text{distância percorrida em dt}}{\text{Número de colisões em dt}} = \frac{v \Delta t}{\pi d^2 v \Delta t N/V} = \frac{1}{\pi d^2 N/V}$ 
	- Considera que todas as outras partículas setão paradas
	$Real \Rightarrow \frac{1}{\sqrt{2}\pi d^2 N/V}$ 

[[Energia interna]]
 - Supomos que seja um gás monoâtomico
 - Supomos que a [[Energia]] interna é resultado da energia de translação
	 $$K_{\text{média}} = \frac{3}{2}KT$$
	$\displaystyle E_{int} = \frac{3}{2} nRT$
	
	- Para volume constante
	$Q = nC_v \Delta T$; $C_v$ é uma constante de calor específico molar a volume constante
	$\Delta E_{int} = nC_v \Delta T -W$
	- Para pressão constante
	$Q = nC_p \Delta T$; $C_p$ é uma constante de calor específico molar a pressão constante $C_p$ sempre é maior que $C_v$ 
	$C_v = C_p -R$
	[[Teorema dos graus de liberdade]]

[[Processo adiabático]] para um gás ideal
	Consideremos
	$d E_{int} = Q -PdV$ -> ocorre um pequeno aumento de volume
	- Se a expansão é adiabática
	Q = 0  e $dE_{int} = nC_vdT$
	$ndT = -(\frac{P}{C_v})dV$
	Pdv +VdP = nRdT; R = $C_p -C_v$
	ndT = $\frac{PdV + VdP}{C_p -C_v}$
	$\frac{dP}{P} + \frac{C_p}{C_v}\frac{dV}{V}=0$
	$\int \frac{dP}{P} + \gamma \frac{dV}{V} = 0$
	$\ln P + \gamma \ln V = Constante \Rightarrow P V^\gamma = constante$

[[Expansão isotérmica]]
	implica em $P = nRT \frac{1}{V} = Constante$
	$W = \int_{V_i}^{V_f} PdV = \int_{V_i}^{V_f} \frac{nRT}{V}dV$
	- Como trata-se de uma isoterma
	$W = nrt \int_{V_i}^{V_f} \frac{dv}{V} = nrt \ln V |_{V_i}^{V_f}$ -> $W = nrt \ln \left( \frac{V_f}{V_i}\right)$ 


**[[Equação de Vander Waals]]**
$$\left( P + \frac{n^2a}{V^2} \right)(V-nb)= nRT$$
nb -> Correção do volume de exclusão
$\frac{n^2a}{V^2}$ -> Correção pelas forças entre moléculas

**[[Condução]]**
	$P_{cond} = \frac{Q}{t} = kA \frac{T_Q-T_c}{L}$
	-> Q é a energia transferida da fonte quente para a fonte fria
	-> A é a área de contato
	-> L é a largura da placa
	-> K é a condutividade térmica do material da placa
[[Resistência térmica]]
	$R = L/k$ -> Resistência a transmitir calor