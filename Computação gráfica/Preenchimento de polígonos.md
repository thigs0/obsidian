- Tema de [[rasterização]]
- Objetivo: determinar quais pixels na tela devem ser coloridos


***Por varredura***
- Definimos uma variável de bit 0
Quando queremos preencher a forma, mudamos o bit para 1 e preenchemos, para isso temos os vértices e definimos com base neles se estamos no interior ou não

**Problemas**
- Dificuldade em analisa formas pontiagudas
- Dificuldade em formas com auto-intersecção

```julia
using Plots

screen = ones(500, 500)
poli = [50 100;
		100 100;
		50 150;
		100 150]
bit = 0
function range(x)
	xmin, xmax= minimum(poli[:, 1]), maximum(poli[:, 1])
	ymin, ymax= minimum(poli[:, 2]), maximum(poli[:, 2])
	
	for j = 1:size(screen)[2]
		if x >= xmin && x <= xmax && j >= ymin &&  j<= ymax
			screen[x, j] = 30
		end
	end
end

anim = @animate for x = 1:size(screen)[1]
	range(x)
end
gif(anim, "test.gif', fps=2)

heatmap(screen, color= :greys)
```


#### [[Preenchimento Scanline]]
- Usamos linhas horizontais, se movendo da parte inferior até a superior
- Em cada linha verificamos se há intersecção com as bordas do [[Polígono]]s
- Quando uma linha da varredura cruza com uma borda poligonal, o algoritmo determina a regiao entre pares de intersecção e a preenche com cor
- **Tabela de Borda (ET):** A tabela de arestas contém todas as arestas do polígono nas listas. cada lista corresponde a uma linha de varredura específica e as bordas da lista são ordenadas com base nos valores Ymin das bordas
- **Lista Ativa (AL):** A lista ativa é responsável por acompanhar as arestas atuais que estão sendo usadas para preencher o polígono. As bordas são adicionadas à lista ativa na tabela de bordas quando seu valor Ymin corresponde à linha de varredura atual. A lista ativa atualiza após o processamento de cada linha
**Ideia do algoritmo**
- Processamos cada arresta do polígono e armazenamos suas informações na tabela de arestas. As informações incluem $ymax,xofYmin$ e SlopeInverse de cada borda
- As arestas são ordenadas com base em seus valores de ymin. Dentro de cada linha de varredura, as bordas são classificadas por seus xofYmin usando classificação por intersecção
#### **Exemplo**
Queremos preencher o 
```
Y ↑
6 |     B(6,6)
5 |
4 |
3 |
2 | A(2,2)-------C(10,2)
  +------------------------> X
    2   4   6   8   10
```

1) **Construir a Edge Table(ET)**
Como começamos na linha 2. Temos os vétices das arestas $\overline{AB}$ e $\overline{CB}$ e assim adicionamos na ET. o critério técnico é $Y_{min}=\text{linha de varredura atual}$ -> é inserida na ET

- $dx$ é o inverso da inclínação $dx=\frac{1}{m}=\frac{x_1-x_0}{y_1-y_0}$ 

| posição ET | $y_{max}$ | $x$ | $dx$                  |
| ---------- | --------- | --- | --------------------- |
| 2          | 6         | 2   | $\frac{6-2}{2-2}=1$   |
| 2          | 10        | 10  | $\frac{6-10}{6-2}=-1$ |
2) **Inicia AL**
- Adicionamos à Al todas as arestas da ET acima
- Removemos da AL arestas com $y_{max} = y$
- Ordenamos a AL por $x$
- Preenchemos os pixels entre pares de $x$
- incrementamos $y$, atualizamos $x$ das arestas $x+=dx$
AL = [x=2 com ymax=6,x=10 com ymax =6]
2) **Iniciamos o algoritmo em y=2**
- Usamos a ET acima
- ordenando por $x$: Preenchemos pixels x=2 até 10
Nossa imagem fica
```
Y ↑
6 |           B
5 |
4 |
3 |
2 |   A###############C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
E atualizamos o x da ET

| posição ET | $y_{max}$ | $x$              | $dx$                  |
| ---------- | --------- | ---------------- | --------------------- |
| 2          | 6         | $x=x_{old}+dx=3$ | $\frac{6-2}{2-2}=1$   |
| 2          | 10        | $x=x_{old}+dx=9$ | $\frac{6-10}{6-2}=-1$ |

3) **Iniciamos o algoritmo em y=3**
- Não temos nenhum vértice a ser adicionado $y_{\text{vértice}}=\text{y varredura}$
- x já está ordenado
- Preenchemos pixels x=3 até 9
```
Y ↑
6 |           B
5 |
4 |
3 |     #############
2 |   A###############C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
E atualizamos o x da ET

| posição ET | $y_{max}$ | $x$              | $dx$                  |
| ---------- | --------- | ---------------- | --------------------- |
| 2          | 6         | $x=x_{old}+dx=4$ | $\frac{6-2}{2-2}=1$   |
| 2          | 10        | $x=x_{old}+dx=8$ | $\frac{6-10}{6-2}=-1$ |

4) **Iniciamos o algoritmo em y=4**
- Não temos nenhum vértice a ser adicionado $y_{\text{vértice}}=\text{y varredura}$
- x já está ordenado
- Preenchemos pixels x=4 até 8
```
Y ↑
6 |           B
5 |
4 |       #########
3 |     #############
2 |   A###############C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
E atualizamos o x da ET

| posição ET | $y_{max}$ | $x$              | $dx$                  |
| ---------- | --------- | ---------------- | --------------------- |
| 2          | 6         | $x=x_{old}+dx=5$ | $\frac{6-2}{2-2}=1$   |
| 2          | 10        | $x=x_{old}+dx=7$ | $\frac{6-10}{6-2}=-1$ |
5) **Iniciamos o algoritmo em y=5**
- Não temos nenhum vértice a ser adicionado $y_{\text{vértice}}=\text{y varredura}$
- x já está ordenado
- Preenchemos pixels x=5 até 7
```
Y ↑
6 |           B
5 |         #####
4 |       #########
3 |     #############
2 |   A###############C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
E atualizamos o x da ET

| posição ET | $y_{max}$ | $x$              | $dx$                  |
| ---------- | --------- | ---------------- | --------------------- |
| 2          | 6         | $x=x_{old}+dx=5$ | $\frac{6-2}{2-2}=1$   |
| 2          | 10        | $x=x_{old}+dx=7$ | $\frac{6-10}{6-2}=-1$ |
6) **Iniciamos o algoritmo em y=6**
- Agora temos o caso $y=y_{max}$ em algum dos vértices do ET, então iremos remover
- Como a ET ficou vazia, o algoritmo termina

#### Exemplo
```
Y ↑
6 |       B            F
5 |             D
4 |            
3 |
2 |   A       C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
Queremos preencher e para isso temos a imagem acima com a seguinte order A->B->D->F->C->A
1) **Construir a Edge Table(ET)**
- Adicionamos todas as arestas menos as horizontais, então
- Adicionamos $\overline{AB}$, $\overline{BD}$, $\overline{DF}$ e $\overline{FC}$ 
- $\overline{AB}=\begin{cases}y_{min} =2\\ y_{max}=6\\ x=2\\ m=0.5\end{cases}$
- $\overline{BD}=\begin{cases}y_{min}=5\\ y_{max}=6\\ x=7\\ m=-3\end{cases}$
- $\overline{DE}=\begin{cases} y_{min}=5\\ y_{max}=6\\ x=7\\ m=0.33 \end{cases}$
- $\overline{EC}=\begin{cases} y_{min}=2\\ y_{max}=6\\ x=6\\m=1 \end{cases}$

| posição ET | $y_{max}$ | $x$ | $dx$  |
| ---------- | --------- | --- | ----- |
| 2          | 6         | 2   | $0.5$ |
| 2          | 6         | 6   | 1     |
| 5          | 6         | 7   | -3    |
| 5          | 6         | 7   | 0.33  |
2) **Inicia AL**
- Adicionamos à Al todas as arestas da ET acima
- Removemos da AL arestas com $y_{max} = y$
- Ordenamos a AL por $x$
- Preenchemos os pixels entre pares de $x$
- incrementamos $y$, atualizamos $x$ das arestas $x+=dx$

2) **Inicia Com y=2*
- Criamos nossa ET e AL

| posição ET | $y_{max}$ | $x$ | $dx$  |
| ---------- | --------- | --- | ----- |
| 2          | 6         | 2.5 | $0.5$ |
| 2          | 6         | 7   | 1     |
$AL=[(6,2,0.5), (6,6,1)]$
2) **Iniciamos com y=3**
- Assim preenchemos de x=2 até x=7
```
Y ↑
6 |       B            F
5 |             D
4 |            
3 |   ###########
2 |   A       C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
- Atualizamos o x na nossa ET e AL

| posição ET | $y_{max}$ | $x$                 | $dx$  |
| ---------- | --------- | ------------------- | ----- |
| 2          | 6         | $x=x_{old}+0.5=2.5$ | $0.5$ |
| 2          | 6         | $x=x_{old}+1=7$     | 1     |
$AL=[(6,2.5,0.5), (6,7,1)]$
4) **inicia com y=4
- Nenhum vértice entra na ET e nem sai
- Preenchemos de X=3 até 8
```
Y ↑
6 |       B            F
5 |             D
4 |     ###########     
3 |   ######### 
2 |   A       C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
- Atualizamos o x na nossa ET e AL

| posição ET | $y_{max}$ | $x$                 | $dx$  |
| ---------- | --------- | ------------------- | ----- |
| 2          | 6         | $x=x_{old}+0.5=3.5$ | $0.5$ |
| 2          | 6         | $x=x_{old}+1=9$     | 1     |
$AL=[(6,3.5,0.5), (6,9,1)]$
5) **iniciamos com y=5**
- Insere na ET os vértices de 6

| posição ET | $y_{max}$ | $x$ | $dx$  |
| ---------- | --------- | --- | ----- |
| 2          | 6         | 3.5 | $0.5$ |
| 2          | 6         | 9   | 1     |
| 5          | 6         | 7   | -3    |
| 5          | 6         | 7   | 0.33  |
$AL=[(6,3,0.5), (6,8,1),(6,7,-3),(6,7,0.33)]$
e ordenamos por x
e temos a ordem 3.5 até 7, 7 até 9

```
Y ↑
6 |      #B##### #### F
5 |     ########D##
4 |   ###########     
3 |   ######### 
2 |   A       C
  +------------------------> X
    1 2 3 4 5 6 7 8 9 10 11
```
- Atualizamos o x na nossa ET e AL

| posição ET | $y_{max}$ | $x$                 | $dx$  |
| ---------- | --------- | ------------------- | ----- |
| 2          | 6         | $x=x_{old}+0.5=3.5$ | $0.5$ |
| 2          | 6         | $x=x_{old}+1=9$     | 1     |
$AL=[(6,3.5,0.5), (6,9,1)]$
6) **Iniciamos com y=6*
- Esvaziamos a ET e AL