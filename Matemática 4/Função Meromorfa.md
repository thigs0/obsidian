Uma função é dita **Meromorfa** em um domínio $D$ e é [[Função analítica]] exceto nos polos

###### Teorema
Seja C um caminho orientado positivamente e suponha que
1. a função f(z) é meromorfa em um domínio interior em C
2. f(z) é analítica e diferente de zero em C
3. Z é um número de zeros e P o número de polos de $f(z)$ dentro de C
Então $$\frac{1}{2\pi}\Delta_C\arg f(z)=Z-P$$
**Demonstração**
Calculamos a [[Integral]] $\displaystyle \int_c \frac{f'(z)}{f(z)}dz=\int_a^b \frac{f'[z(t)]z'(t)}{f[z(t)]}dt$ 
Podemos parametrizar a função como $f(z(t))=\rho (t)e^{i\phi(t)}$ 
Assim, temos $\displaystyle f'(z(t))z'(t)=\rho'(t)e^{i\phi(t)}+i\rho(t)e^{i\phi(t)}\phi'(t)$
e avaliamos duas integrais
$\displaystyle \int_a^b \frac{\rho'(t)}{\rho(t)}dt+i\int_a^{b} \phi'(t)dt$ Como a primeira integral é de função [[Holomorfa]], resulta em 0, e a integral de $\phi'$ leva ao ramo da função com [[Logaritmo]]. Então
$$\int_C\frac{f'(z)}{f(z)}dz=i\Delta_C\arg f(z)$$
**Corolário**
Como a função tem zeros de ordem $m_0$ podemos reescrever $f(z)$ na forma
$f(z)=(z-z_0)^{m_0}g(z)$ Se $g(z)$ é diferente de 0,
$f'(z)=m_0(z-z_0)^{m_0-1}g(z)+(z-z_0)^{m_0}g'(z)$
=> $\displaystyle \frac{f'(z)}{f(z)}=\frac{m_0}{z-z_0}+\frac{g'(z)}{g(z)}$ Como a fração de $g(z)$, supomos que ela tem polos de ordem até $-m_p$. Então conseguimos reescrever da forma
$g(z)=(z-z_0)^{-m_p}\phi(z)$,
$g'(z)=-m_m(z-z_0)^{-m_p-1}\phi(z)+(z-z_0)^{-m_p}\phi'(z)$ 
=> $\displaystyle \frac{f'(z)}{f(z)}=\frac{m_0}{z-z_0}+\frac{-m_p}{z-z_0}+\frac{k'(z)}{k(z)}$ Agora temos que f(z) é [[Holomorfa]], então quando integramos e aplicamos o teorema dos resíduos, obtemos
$$\int_c\frac{f'(z)}{f(z)}dz=2\pi i(Z-P)~~~\begin{cases}\text{Z é a ordem dos zeros}\\ \text{P é a ordem dos Polos}\end{cases}$$
