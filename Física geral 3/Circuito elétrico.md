- Os elétrons não são consumidos em nenhuma parte do circuito, eles transportam energia, e ela que é consumida
	- A corrente se conserva
	- A dissipação de energia em um fio é ignorada por todo ponto em um ﬁo está essencialmente no mesmo potencial.

#### Modelo Drude 
Considere um fio condutor e que os elétrons livres estão sobre um [[Campo elétrico]]. A velocidade deles é $\displaystyle \vec v= \vec v_0 - \frac{-e\vec E}{m_e}\Delta t$

Tomando a velocidade média $\displaystyle \vec v_d = \frac{e\vec E}{m_e} \tau$; em que $\tau$ é o intervalo médio entre colisões

J é a densidade de corrente, $\vec J \equiv \frac{|i|}{A} = nq\vec v_d$ . Aplicamos a velocidade e obtemos
$\displaystyle \vec J = \frac{ne^2\tau}{m_e} \vec E$; o termo constante é chamado de $\sigma \equiv$ condutividade do material

$\displaystyle \sigma = \frac{J}{E} \left[ \frac{A}{m^2} \right]$

#### [[Resistência]]

A resistência é definida como $$R \equiv \frac{V}{I} \left[ \Omega \right]$$
A fórmula acima é equivalente a $\displaystyle R = \frac{l}{\sigma A}$
Se as resistências são paralelas, temos
$$\frac{1}{R_t}=\frac{1}{R_1}+\frac{1}{R_2}+\frac{1}{R_3}+...$$
Se as resistências são em série, temos
$$R_t=R_1+R_2+R_3+...$$

- A resistência é sempre positiva

###### Potência dissipada por uma resistência
	$$P = I^2R$$

### Regra da malha
- ao avaliar a malha temos a conservação de energia dada por $\displaystyle \sum \xi + \sum V =0$; (estado estacionário de uma espira)
- Caimos em uma [[Equação Diferencial linear de coeficiente constante]]



```circuitjs
$ 1 0.000005 10.20027730826997 50 5 43 5e-11
r 176 80 384 80 0 10
s 384 80 448 80 0 1 false
w 176 80 176 352 0
c 384 352 176 352 0 0.000015 -9.16123055990675 -10
l 384 80 384 352 0 1 -0.01424104005209455 0
v 448 352 448 80 0 0 40 5 0 0 0.5
r 384 352 448 352 0 100
o 4 64 0 4099 20 0.05 0 2 4 3
o 3 64 0 4099 20 0.05 1 2 3 3
o 0 64 0 4099 0.625 0.05 2 2 0 3
38 3 F1 0 0.000001 0.000101 -1 Capacitance
38 4 F1 0 0.01 1.01 -1 Inductance
38 0 F1 0 1 101 -1 Resistance
h 1 4 3
```



- ## Circuito RC e RCL em série
	- 