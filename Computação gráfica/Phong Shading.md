- É um sombreamento de interpolação por [[Vetor]] normal
- Melhora o [[Gouraud shading]] 

1) **Luz de ambiente**
- Simula como se a [[luz]] viesse de todas direções, não depende da lâmpada
$$I_{ambiente}=K_a.I_a;~~\begin{cases} K_a~ \text{Coeficiente ambiente do material}\\ I_a~ \text{Intensidade da luz de ambiente} \end{cases}$$
2) **Luz difusa**
- Depende do ângulo entre o vetor normal e a superfície
$$I_{difusa}=K_d.I_l.\max(0,\vec N\cot \vec L)\begin{cases} K_d~\text{Coeficiente difuso do material}\\ I_l~\text{Intensidade da luz}\\ \vec N\cdot \vec L~\text{Produto escalar entre normal e luz} \end{cases}$$
3) **Luz especular**
- Brilho por reflexão, mais intenso
- $\vec R=2(\vec N\cdot \vec L)\vec N-\vec L$ 
$$I_{especular}=K_s.I_l.\max(0,\vec R\cdot \vec V)^n~\begin{cases} K_s~\text{Coeficiente especular do material}\\ n~\text{Intensidade do brilho}\\ \vec R\cdot \vec V ~\text{produto escalar reflexão da luz e câmera}\end{cases}$$

Observando com comportamento de cada componentes de ambiente, difusão e especular
![[960px-Phong_components_version_4.png|600]]

#### Exemplo
queremos calcular para o ponto $p=(1,1,1)$, com a normal sendo $N=(0,1,0)$ e a luz $L=(5,5,0)$, Câmera $V=(0,2,5)$, intensidade da luz $I_l=(1,1,1)$
com $K_a=0.1,~~K_d=0.7,~~K_s=0.5,~~n=16$
$\hat{L}=||L-P||=||(4,4,-1)||=\frac{1}{\sqrt{33}}(4,4,-1)$
$\hat V=||V-P||=||-1,1,4||=\frac{1}{\sqrt{18}}(-1,1,4)$
**Calcular a luz ambiente**
$I_a=K_a.I_l=0.1(1,1,1)=(0.1,0.1,0.1)$
**Calcular a luz difusa**
$\vec N\cdot \vec L=(0,1,0)\cdot \frac{1}{\sqrt{33}}(4,4,-1)=\frac{4}{\sqrt{33}}$ 
$I_{difusa}=K_d.I_l.\max(0,\vec N\cdot \vec L)=0.7.(1,1,1).\frac{4}{\sqrt{33}} =\frac{1}{\sqrt{33}}(2.8,2.8,2.8)$
**Calcular a luz especular**
Reflexo, $\vec R =2(\vec N\cdot \vec L)\vec N-\vec L=2.\frac{4}{\sqrt{33}}(0,1,0)-\frac{1}{\sqrt{33}}(4,4,-1)=(-0.696,0.696,0.174)$ 
$\hat R=(-0.694,0.694,0.173)$
$\vec R\cdot \vec V=0.654$
$I_{especular}=K_s.I_l.(\max(0,\vec R\cdot \vec V))^n=0.5.(1,1,1).0.654^{16}=(0.000365,0.000365,0.000365)$
**Iluminação final**
$I=I_{amb}+I_{difusa}+I_{especular}=(0.587,0.587,0.587)$


