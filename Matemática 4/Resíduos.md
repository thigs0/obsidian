Quando $z_0$ é um ponto singular isolado da função f, há um número positivo $R_2$ tal que a função f analítica em cada ponto para $0 < |z-z_0|<R_2$. Consequentemente $f(z)$ tem representação em [[Série de Leurent]]
$$f(z) = \sum_{n=0}^{\infty}a_n(z-z_0)^{n}+ \frac{b_1}{z-z_0}+\frac{b_2}{(z-z_0)^2}+...+\frac{b_n}{(z-z_0)^n}+...$$
Quando n=1, a expressão para o $b_n$ é
$$b_n = \frac{1}{2\pi i}\int_c f(z)dz$$
Mas como o objetivo e calcular a integral que pode ser complicada,
$$\large\int_c f(z)dz = 2\pi i b_n$$
Quando temos $b_1$ que acompanha o termo $a/(z-z_0)$ na expansão, chamamos de resíduo.
$$\large b_1 = Res_{z=z_0}f(z)$$
- Serve para avaliar integrais complexas com singularidades

 ---
 Exemplos
 Calcule $\displaystyle \int_c \frac{e^z-1}{z^4}dz$.

Primeiro representamos a função em série de potências
$\displaystyle \frac{e^z-1}{z^{4}}= \frac{1}{z^4}(e^z-1)$ Como A expansão do exponencial no primeiro termo é 1, que anula com o -1, começamos em 1.
$\displaystyle \frac{1}{z^4} \sum_{n=1}^\infty \frac{z^n}{n!} =\sum_{n=0}^\infty \frac{z^{n-4}}{n!}$ Quando n=3, obtemos uma singularidade e seu coeficiente é $1/3! = 1/6$ 
Então $\displaystyle \int_{c} \frac{e^z-1}{z^4} = 2\pi i \left(\frac{1}{6}\right) = \frac{\pi i}{3}$
  
---

#### [[Teorema do resíduo de Chauchy]]
Seja C uma curva simples descrita positivamente. Seja f uma [[Função analítica]] dentro e em uma curva C com finitos elementos irregulares $z_k(k=1,2,3,...)$ dentro de C, então
$$\int_c f(z)dz= 2 \pi i\sum_{k=1}^{n} Res f(z_k)$$
	Prova:
	Considerando as condições de hipóteses, temos o [[Teorema de Cauchy-Goursat]], que nos garante 
	$$\int_c f(z)dz~~ -\sum_{k=1}^{n} \int_{c_k} f(z)dz =0$$
	Pela teoria dos resíduos, temos que $$\int_cf(z)dz=2 \pi iRes(z_0)$$
	o que já demonstra o teorema.
