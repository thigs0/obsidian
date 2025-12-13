Seja $X=(X_1,...,X_p)$ um [[Vetor aleatório]] p-dimensional, a [[Função geradora de momento]] é definida como sendo
$$M_X(t)=\mathbb{E}(e^{t_1X_1+t_2X_2+...+t_pX_p})$$
Em particular para **p=2**
$M_X(t_1,t_2)=\mathbb{E}(e^{t_1X_1+t_2X_2})$, caso bivariado

***Exemplo 1***
$X_1$~$N(\mu_1,\sigma_1^2)$ e $X_2~N(\mu_2,\sigma_2^2)$ com [[Independência]]. Queremos obter a distribuição $Z=X_1+X_2$ via FGM
$M_Z(t)=\mathbb{E}(e^{t(X_1+X_1)})=\mathbb{E}(e^{tX_1}e^{tX_2})=\mathbb{E}(e^{tX_1})\mathbb{E}(e^{tX_2})=M_{X_1}(t)M_{X_2}(t)=e^{t\mu_1+\frac{\sigma_1^2}{2}t^2}.e^{t\mu_2+\frac{\sigma_2^2}{2}t^2}$
$=e^{t(\mu_1+\mu_2)+\frac{\sigma_1^2+\sigma_2^2}{2}t^2}\Rightarrow Z=X_1+X_2$~ $N(\mu_1+\mu_2,\sigma_1^2+\sigma_2^2)$ 

