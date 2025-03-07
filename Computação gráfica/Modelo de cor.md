
[[Imagem]]
é uma [[Matriz]] bidimensional com valores variando com a intensidade da cor representada, sua profundidade pode respresentar as cores

Escalas de cor é dada pelo seu tamano [[Bits]]
![[Gradient-Bit-Depth-Test-File-Greg-Benz-1.jpg]]

**[[Tamanho de uma imagem]]**
é q quantidade de linhas e quantidade de colunas

**[[Resolução da imagem]]**
Quantidade de pixel no mundo real que irá representar a imagem

### RGB
é uma modelagem de um espaço de cores, onde cada ponto é dado por
$P_0=(R\hat i, G\hat j, B\hat k)$ tal que $\hat i,\hat j,\hat k$ são espaçadas pelos [[Bits]] usados
![[colorcube.jpeg]]
**Escala de cinza** ocorre quando tomamos $R=G=B$ 

**Conversão para cinza**
$$Y=Avg(R,G,B)=\sum\limits_{i=R,G,B} a_i i$$
em que $a_i$ são os pesos usados que podem variar conforme o problema

### HSL
usa [[coodenada cilíndrica]] como base
Considera as cores, brilho e saturação

### CMYK
- Modelo voltado para impressoras por ser subtrativo, quanto maior a intensidade mais escuro a cor