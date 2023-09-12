**[[Equações de Maxwell]]**
$$\displaystyle \begin{cases} div ~\vec E =0\\ Rot~\vec E = -\frac{1}{c}\frac{\partial H}{dt}\\ div~ \vec H =0 \\ rot ~\vec H = \frac{1}{c}\frac{\partial \vec E}{dt}\end{cases}$$


### Indutância
a [[Indutância]] é a tendência de um condutor elétrico se opor a uma mudança na corrente elétrica que flui por ele. A unidade de [L] é Henry

	$\displaystyle \epsilon_{ind}= -L \frac{di}{dt}$
Quando tratamos de um senoide infinito temos:
$\displaystyle \Phi_\beta = \frac{\mu_oNiA}{L}N \Rightarrow \frac{d\Phi_\beta}{dt}=\frac{\mu_o N^2 A}{L}\frac{di}{dt}$ 

$\displaystyle P = \frac{dw}{dt} = -\epsilon_{ind}\frac{dq}{dt}=L\frac{di}{dt}i=\frac{d}{dt}\left( \frac{1}{2}Li^2\right)$


$\displaystyle W = \frac{1}{2} \frac{\mu_0 N^~2Ai^2}{L}=\frac{1}{2\mu_0}\beta^2 LA$


#### [[Vetor de Pognting]]
	
	$$\vec S = \frac{1}{\mu_0}\vec E \times \vec B$$
	A potência do vetor de pognting é definida como a [[Integral de linha]] do vetor de pognting:
	$\displaystyle P = \oint \vec S \cdot d\vec A$                   # A é a área pela que o vetor 
	
	
	
### Ondas eletromagnéticas
- caso temos uma carga em movimento, talvez em oscilação. O campo gerado por ela é de forma:
$\displaystyle \vec E = \frac{Q}{4\pi \epsilon_0 r^2} \frac{1-\beta^2}{(1-\beta^2* sin(\theta))^{3/2}}$; Tal que $\displaystyle \beta = \frac{v}{c}$

Ao invés de uma carga oscilando, podemos construir duas cargas que trocas de sinal por haver uma corrente entre elas alternada. Com uma corrente, escolhemos uma amperiana.

- Fluxo de energia
	$dU = uAdx$, sendo u a densidade de energia

	$\displaystyle \frac{du}{dt} = uA\frac{dx}{dt} \rightarrow S=\frac{1}{A}\frac{dx}{dt} = uc \rightarrow \vec S = \frac{1}{\mu_0} \vec E \times \vec B$

#### Campo magnético em um fio
![[Campo_fio.png|400]]
- A corrente elétrica causa um campo magnético
	$$\beta = \frac{\mu_0 i}{2\pi d};\hspace{1cm}d=\text{distância do fio},~\mu=$$
#### Campo magnético em um senóide
![[campo_bobina.png|500]]
é dado por $$\beta = \frac{\mu_0 Ni}{L}\hspace{1cm}\begin{cases}i= \text{Corrente elétrica}\\ L=\text{Corrente elétrica}\\N=\text{Número de espiras}\end{cases}$$