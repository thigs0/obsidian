Seja $X_1,X_2,...$ uma [[Cálculo 3/Sequência|Sequência]] de [[Variável Aleatória]]s independentes e identicamente distribuídas, cada uma com média $\mu$ e variância $\sigma^2$. Então, a distribuição de
$$\frac{X_1+...+X_n-n\mu}{\sigma \sqrt{n}};~~~~~\frac{\overline X -\mu}{\sigma/\sqrt{n}}$$
tende à [[Distribuição normal]] padrão quando $n\to\infty$. Isto é, para $-\infty < a<\infty$,
$$P\left[ \frac{X_1+...+X_n-n\mu}{\sigma \sqrt{n}}\leq a \right]\to \frac{1}{\sqrt{2\pi}}\int_{-\infty}^a e^{-x^2/2}dx~~~~quando~~~~n\to \infty$$
**Lema 1**
Seja $Z_1,Z_2,...$ uma [[Cálculo 3/Sequência|Sequência]] de variáveis aleatórias com [[Funções]] distribuição $F_{Z_n}$ e [[Função geratriz]] de momentos $M_{Z_n}n\geq 1$; Seja também Z uma variável aleatória com função distribuição $F_z$ e função geratriz de momento $M_Z$. Se $M_{Z_n}(t)\to M_Z(t)$ para todo t, então $F_{Zn}(t)\to F_z(t)$ para todo t no qual $F_Z(t)$ é [[Contínua]]

- A soma de um grande número de [[Variável Aleatória]]s independentes tem distribuição que é aproximadamente normal

**Propriedades convergência em probabilidade**
1. $X_n+Y_n\xrightarrow P X+Y$
2. $X_nY_n\xrightarrow P X.Y$
3. $a_n.X_n\xrightarrow P aX$
4. $g(X_n)\xrightarrow P g(X)$

**Propriedades convergência em distribuição**
1. $X_n+Y_n\xrightarrow D X+Y$
2. $Y_nX_n\xrightarrow D X.Y$
3. $a_nX_n\xrightarrow D aX$
4. $g(X_n)\xrightarrow D g(X)$

**observação**
1. $X_n\xrightarrow{qe} X\Rightarrow X_n\xrightarrow D X$ 
2. $X_n\xrightarrow D \lambda \Rightarrow X_n\xrightarrow D X$
3. $X_n\xrightarrow D C\Rightarrow X_n\xrightarrow D C$, C é constante