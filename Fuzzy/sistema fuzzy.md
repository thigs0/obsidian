é aplicado em 
- automação e controle
- previsão de [[série temporal]]
- reconhecimento de padrões
- [[Biomatemática]]

Existem sempre três componentes
1) **Dicionário** que define o conjunto fuzzy sobre as variáveis
2) **Base de regras** que estabelece uma relação entre as variáveis
3) **Método de inferência** usado para determinar a saída dado uma certa entrada

**[[método de inferência de Mandani]]**
O [[conjunto fuzzy]] da quantidade é determinado através da união dos conjuntos fuzzy obtido tomando o mínimo entre $w_i$ e a [[Função de pertinencia]] do consequente regra, ou seja
$$\varphi_\text{Qtd}=\cup_{i=1}^n (W_i\land\varphi_{Q_i})$$

### Exemplo com Lava Roupas
- Objetivo é automatizar o funcionamento de uma máquina de lavar roupas de modo que iremos economizar água, eletricidade e detergente.
- Variáveis independentes são **peso** e **sujeira**
- Variáveis dependentes são **Quantidade de detergente**
$$\text{Peso}=\begin{cases}\text{Muito leve}\\ \text{Leve}\\ \text{Pesado}\\ \text{Muito pesado}\end{cases}= \begin{cases}\varphi_\text{Muito leve}(p)=T(-20,-10,0,20)\\ \varphi_\text{Leve}(p)=T(10,30,50)\\\varphi_\text{Pesado}(p)=T(40,65,90)\\ \varphi_\text{Muito pesado}(p)=T(75,90,100,120)\end{cases}$$  
$$\text{Qtd Detergente}=\begin{cases}\text{quase limpo}\\ \text{sujo}\\ \text{muito sujo}\\ \text{extra sujo}\end{cases}= \begin{cases}\varphi_\text{qquase limpo}(p)=T(-20,0,20)\\ \varphi_\text{sujo}(p)=T(10,30,50)\\\varphi_\text{muito sujo}(p)=T(40,70,100)\\ \varphi_\text{extra sujo}(p)=T(80,100,120)\end{cases}$$
**Tabela de regras fuzzy para o gasto de detergente**

|              | Quase limpo | Sujo      | Muito sujo | Extra sujo |
| ------------ | ----------- | --------- | ---------- | ---------- |
| Muito Leve   | Muito pouco | Pouco     | Moderado   | Moderado   |
| Leve         | Pouco       | Pouco     | Moderado   | Exagerado  |
| Pesado       | Moderado    | Moderado  | Exagerado  | Exagerado  |
| Muito pesado | Moderado    | Exagerado | Máximo     | Máximo     |

- Usarei o [[método de inferência de Mandani]]
Dado o peso é $p=10$ e o nível de sujeira é $s=15$, determinamos a quantidade de detergente
$$W_i=\varphi_{A_i}(p)\land \varphi_{A_{2i}}(s),~\forall i=1,2,...,16$$
$$\begin{align} W_1 = \varphi_\text{Muito Leve}(p)\land \varphi_{\text{Quase limpo}}(s)=0.5\land 0.25=0.25\\ W_2=\varphi_\text{Muito leve}(p)\land \varphi_\text{sujo}(s)=0.5\land 0.25=0.25 \end{align}$$

![[maquinaLavar.png]]