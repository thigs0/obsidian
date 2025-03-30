Neste modelo as regras são da forma 
Se $x_1$ é $A_{1i}$ e $x_2$ é $A_{2i}$ ... então $y=f_i(x_1,x_2,x_3,...,x_n)$
em que $A_{1i}, A_{2i},...A_{ni}$ são um [[conjunto fuzzy]] dos antecessores enquanto que o consequente é uma [[função]] das variáveis de entrada
- Temos que geralmente $f_i$ são polinômios
- Temos que um modelo de Takagi-sugeno de ordem zero se $f_i$ são constantes
- Temos que se um modelo de Takagi-Sugeno de ordem um se $f_i$ são polinômios de ordem 1
**Inferencia de takagi-Sugeno**
$$y=\frac{\sum\limits_{i=1}^k W_i f_i(x_1,x_2,...x_n)}{\sum\limits_{i=1}^kW_i}$$
em que $$W_i=\varphi_{A_{1i}}(x_1)\Delta \varphi_{A_{2i}}(x_2)\Delta...\Delta \varphi_{A_{ni}}(x_n),~\forall i=1,2,...,k$$
### Exemplo: Lava-loupas
- **Objetivo:** Automatizar o funcionamento de uma máquina de lavar de modo a economizar água, eletrecidade e detergente
- **Variáveis independentes:** Peso e sujeira
- **variáveis dependentes:** Quantidade de detergente
$$\text{Fuzzificação do peso} \rightarrow \begin{cases}\varphi_{\text{Muito Leve}}(x)=T(-\infty,0,20)\\ \varphi_{\text{Leve}}(x)=T(10, 30,50)\\ \varphi_{\text{Pesado}}(x)=T(40,63,90)\\ \varphi_{\text{Muito Pesado}}(x)=T(75,90,\infty)\end{cases}$$
$$\text{Fuzzificação da sujeira} \rightarrow \begin{cases}\varphi_{\text{quase limpo}}(x)=T(-\infty,0,20)\\ \varphi_{\text{pouco sujo}}(x)=T(10, 30,50)\\ \varphi_{\text{sujo}}(x)=T(40,63,100)\\ \varphi_{\text{Muito Sujo}}(x)=T(80,100,\infty)\end{cases}$$

Neste ponto, escolhemos constantes para delimitar as variáveis independentes de modo a formarem triangulares próprias

![[./imagem/ind_var_sugeno.png|400]]

- construindo a [[Base de regras]] com 16 regras no total

| f            | Quase limpo | Quase limpo | Muito sujo | Extra. sujo |
| ------------ | ----------- | ----------- | ---------- | ----------- |
| Muito Leve   | Muito pouco | Pouco       | moderado   | moderado    |
| Leve         | Pouco       | Pouco       | Moderado   | Exagerado   |
| Pesado       | Moderado    | Moderado    | Exagerado  | Exagerado   |
| Muito pesado | Moderado    | Exagerado   | Máximo     | Máximo      |
- Supomos que estamos no caso $\begin{align}p=10;~\text{sendo o nível de sujeira}\\ s=15;~\text{sendo a quantidade de detergente}\end{align}$
- Calculamos a ativação $W_i=\phi_{A_{1i}}(p) \wedge \phi_{A_{2j}}(s),~~ \forall i=1,2,...,16$
- Por fim, a quantidade y de detergente é determinada somando o produto da ativação pelo consequente da regra e dividindo o resultado pelo soma das ativações, ou seja
$$y=\frac{\sum\limits_{i=1}^{16} W_i Q_i}{\sum\limits_{i=1}^{16}W_i}$$
### Exemplo de [[Cálculo numérico/Quadrados mínimos|Quadrados mínimos]]
