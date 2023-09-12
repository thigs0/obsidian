Podemos aproximar por pela ![exponencial](http://www.dca.iag.usp.br/material/morales/ACA412/Aula_Radar_05_Relacao_ZR.pdf) [[Distribuição exponencial]]
$$N(D) = N_0e^{-\lambda D}$$
$N_0$ sendo uma constante normalmente $8.10^6 m^{-4}$
$D$ é o diâmetro da gota (aproximamos ela como esférica) ($m$)
$\lambda$ é o coeficiente angular ($m^-1$) 

Sabendo que a fórmula é $\displaystyle Z = \int_0^\infty N(D)D^6dD$
aplicamos e fazemos (*) $\displaystyle \int_0^\infty N_0 e^{-\lambda D}D^6dD= N_0 \int_0^\infty e^{-\lambda D}D^6dD$ 

Podemos verificar que é a [[Função Gamma]] $\displaystyle \Gamma(1) = \frac{N_0}{\Gamma(1)}x^{1-1}e^{-\alpha x}$
fazendo uma mudança de variável temos $N_0 \int_0^\infty x^{v-1}e^{-ux}dx$ e obtemos $\displaystyle \frac{\Gamma(v)}{u^v}$ -> v=7, u=$\lambda$ 
