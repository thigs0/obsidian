É uma técnica para descobrir um intervalo que contém os [[Autovalor]]es 

Seja $A\in \mathbb{C}^{n\times n}$ e seja $R_i$ a soma dos termos da linha $i$ com exceção da diagonal 
$$R_i=\sum_{j\neq i}|a_{ij}|$$
Conseguimos construir um disco fechado com centro $a_{ii}$ e raio $R_i$ $D(a_{ii}, R_i)\subset \mathbb{C}$, de modo que todos autovalores estão contidos em pelo menos um dos discos
### Prova
Seja $\lambda_j$ um [[Autovalor]] associado a [[Matriz]] A correspondendo ao [[Autovetor]] $v_j$ 
Este autovetor tem suas componentes $x_1,x_2,x_3,...,x_n$, escolhemos o índice $i$ tal que $|x_i|\geq |x_j|, i\neq j$ 
Com o problema característico
$$Av_j=\lambda v_j$$
Analisamos o i-ésima linha
$$\sum_{j=1}^n a_{ij}x_i=\lambda x_i$$
Então passamos o termo da diagonal $a_{ii}$ para direita 
$$\sum_{j\neq i}a_{ij}x_j= (\lambda-a_{ii})x_i\Rightarrow \sum_{j\neq i}a_{ij}\frac{x_j}{x_i}=\lambda -a_{ii}$$
como escolhemos $x_i$ sendo o maior componente, $x_j /x_i\leq 1$ 
Aplicamos a [[Desigualdade triangular]] 
$$|\lambda-a_{ii}|=\left| \sum_{j\neq i} a_{ij}\frac{x_j}{x_i}\right|\leq \sum_{i\neq j}|a_{ij}|=R_i$$
de forma que $R_i\geq 0$ 

### Exemplo
Tomamos 
$$m = \begin{pmatrix}3 & 1 & -1 & 4 \\ 2 & 1 & 0 & 1 \\ 2 & -3 & -1 & 0 \\ 0 & 6 & -5 & 1\end{pmatrix}$$
temos 
$a_{11}=3$ e $R_1=|1|+|-1|+|4|=6$
$a_{22}=1$ e $R_2=|2|+|+0|+|1|=3$ 
$a_{33}=1$ e $R_3=|2|+|-3|+|0|=5$
$a_{44}=1$ e $R_4=|0|+|6|+|-5|=11$  

Assim, conseguimos construir as esperas e temos uma região limitadora para os [[Autovalor]]es
```mathematica
ContourPlot[{(x-3)^2+(y)^2==6^2, (x-1)^2+(y)^2==3^2, (x-1)^2+(y)^2==5^2, (x-1)^2+(y)^2==11^2},{x,-20,20},{y,-20,20},Axes->True]
```
![[esferas.png|400|center]]


- Função que calcula o intervalo em que temos os autovalores em uma matriz simétrica
```julia
function Gershgorin_sime(A)
	#A função calcula o intervalo em que estão os autovalores de A. Sendo A uma matriz simétrica
	n = size(A)[1]
	resul = zeros(n)
    for i in 1:n
		    for j in 1:n
		        if i != j
				        resul[i] += A[i, j]
		        end
		    end
    end
	#procura o maior e menor valor na diagonal
	ma,me=-10e9,10e10
  
	for i in 1:n
      if A[i, i]+resul[i] > ma
          ma = A[i, i]+resul[i]
      end
      if A[i, i]-resul[i] < me
          me = A[i, i]-resul[i]
		  end
	end

  return(me, ma)
end

```