- A = B+C  ou A = B - C
$$\sigma_A = \sqrt{\sigma_B^2 + \sigma_C^2}$$
- A = BC ou A = B/C
$$\sigma_A = A\sqrt{\left( \frac{\sigma_B}{B} \right)^2 + \left( \frac{\sigma_C}{C}	  \right)^2}$$

| Função                   | Variância                                                | (Nº) |
| ------------------------ | -------------------------------------------------------- | ---- |
| ${\displaystyle f=aA\,}$ | ${\displaystyle \sigma _{f}^{2}=a^{2}\sigma _{A}^{2}}$   | (1)  |
| f = A.B                  | $\sigma_f^2 = \bar A^2 \sigma_B^2 + \bar B^2 \sigma_A^2$ | (2)  |
|                          |                                                          |      |
	Prova (2):
	Seja $\Delta A$ o produto de $(\bar x + \Delta x)$ por $(\bar y + \Delta y)$
	$\Delta \bar A = (\bar x + \Delta x)(\bar y + \Delta y)$ 
	$\Delta A =  \bar {xy} + \bar x \Delta y + \bar y \Delta x +\Delta x \Delta y$
	Aproximamos $\Delta x \Delta y$ como igual a 0
	.
	Agora calculamos $\displaystyle \sigma_A^2 = \frac{1}{n-1}\sqrt{\sum_{i=0}^n(\Delta A_i)^2}$ 
	-> $\displaystyle \frac{1}{n-1}\sum_{i=0}^n (\bar x^2 \Delta y_i^2 + \bar y^2 \Delta x_i^2 + 2\bar {xy} \Delta x_i \Delta y_i)$, Aproximamos novamente $2 \bar {xy} \Delta x_i \Delta y_i =0$
	-> $\displaystyle \sigma_A^2 = \bar x^2 \sigma_y^2 + \bar y^2 \sigma_x^2$
	

**De modo geral**
	$\displaystyle \sigma_f^2 = \sum_{i=0}^n \left (\frac{\partial f}{\partial x_i} \sigma_{x_i}\right)^2$, A incerteza de uma função é a [[Derivada]] da função pela variável vezes a incerteza ao quadrado
	