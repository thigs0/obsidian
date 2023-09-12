## Usando Transformação de givens
Vamos usar a matriz de rotação para simplificar a [[Matriz]] 
$A = \begin{bmatrix} a_{11} & a_{12}\\ a_{21} & a_{22}\end{bmatrix}$
usando a [[Matriz de rotação]] Q, tal que $Q^T \begin{bmatrix}a_{11}\\ a_{21} \end{bmatrix} = \begin{bmatrix} r_{11} \\0\end{bmatrix}$
onde $r_{11} = \sqrt{a_{11}^2 +a_{22}^2}=Q^T \begin{bmatrix}a_{12}\\ a_{22} \end{bmatrix}$ e seja
$\begin{bmatrix} r_{11} & r_{12}\\ 0 & r_{22}\end{bmatrix}$, => $Q^TA=R$ => $QQ^TA = QR$ => $A=QR$

Resolvendo o sistema
$\begin{equation} Ax=B\end{equation}$ => $Q^TAx = Q^Tb$ => $Rx=c$
- Isso significa que só temos que multiplicar $Q^T$ por b e depois resolver um sistema triangular superior.
- $A=QR$, Q [[Matriz ortogonal]], é conhecida como decomposição QR 
$\begin{bmatrix} 1 & 2\\ 1 & 3\end{bmatrix}\begin{bmatrix}z_1 \\z_2 \end{bmatrix} = \begin{bmatrix} 1\\2\end{bmatrix}$

$r_{11} = \sqrt{1^2 + 1^2} = \sqrt{2}$
$\displaystyle cos(\theta)=\frac{1}{\sqrt{1^1+1^2}}$ => $\displaystyle cos(\theta) = \frac{1}{\sqrt{2}}$
$\displaystyle sen(\theta) = \frac{1}{\sqrt{1^2+1^2}}$ => $\displaystyle sen(\theta) = \frac{1}{\sqrt{2}}$ 
...
$\begin{bmatrix} r_{12} \\ r_{22}\end{bmatrix} = Q^T\begin{bmatrix}5/\sqrt{2}\\ 1/\sqrt{2}\end{bmatrix}$


Def: uma rotação de Givens ([[Transformação de Givens]]) é uma rotação no plano gerado por dois eixos de coordenadas
Não nulos da matriz são
$\begin{cases} g_{kk} = 1;~k \neq i,j\\ g_{ii} = cos(\theta) \\ g_{jj}=cos(\theta)\\ g_{ji}=sen(\theta)\\ g_{ij}=-sen(\theta)\end{cases}$

1) $Q_{23}= \begin{bmatrix} 1 & 0 &0 \\ 0 & c & -s\\ 0 & s&c \end{bmatrix}$ é a rotação que ocorre no plano yz.
OBS: Queremos aplicar a matriz de rotação de Givens para através de sucessivas aplicações obter uma matriz triangular superior.
2) $\begin{bmatrix} c & s& 0\\ -s & c & 0\\ 0 & 0&1\end{bmatrix}\begin{bmatrix} a_{11}\\a_{21}\\a_{31}\end{bmatrix}=\begin{bmatrix} *\\ 0\\ \Delta \end{bmatrix}$ aplicamos $Q_{23}$ para anular o segunda termos
**Teorema** 
Seja $A \in \mathbb{R}^{nxn}$. Então existe uma matriz ortogonal Q e uma matriz trianguar superior R, tal que A = QR
	Dem: Seja $Q_{21}$ uma rotação de Givens no plano $x_1x_2$, tal que $$Q_{21}^t\begin{bmatrix} a_{11}\\ a_{21}\\...\\ a_{n1}\end{bmatrix} = \begin{bmatrix} *\\0\\...\\a_{n1}\end{bmatrix}$$
	Observe que a posição (2,1) da matriz $Q_{21}^tA$ é zero. Agora podemos construir $Q_{31}$ atuando em $x_1x_3$, tal que
	$Q_{31}^t(Q_{21}^tA)$ será zero na posição (3,1) 
	Podemos continuar este processo, tal que 
	$Ã = Q_{n1}^t(Q_{n-1,1}^t,...,Q_{21}A)$ tenha zero na posição (n,1)
	Portanto, na 1º coluna de Ã, todos os elementos são zeros, exceto (talvez) o da posição (1,1).
	Agora, vamos trabalhar na segunda coluna de Ã.
	Seja $Q_{32}$ a rotação de Givens que atua no plano $x_2x_3$
	tal que $Q_{32}^tÃ$ tenha entrada (3,2) igual a zero. fazendo isto até o fim desta coluna temos que a segunda coluna de $Q_{32}^t$ ... com entrada todas iguais a zero abaixo $x_0$ do elemento diagonal.
	Continuando com processo até a coluna (n-1), teremos 
	$$Q_{n, n-1}^t.Q_{n, n-2}^t....Q_{21}^tA=R$$
	onde R é uma matriz triangular superior
**Exercício**
	$A=\begin{bmatrix} 1 & 2 &4\\ -1& 2& 1\\ 1 & -1& 3\end{bmatrix}$. Encontre a decomposição QR.
	$k_{11} = \sqrt{(1^2 + (-1)^2)} = \sqrt{(2)}$
	=> $\displaystyle cos(\theta) = \frac{1}{\sqrt{2}}$; $\displaystyle sin(\theta) = \frac{-1}{\sqrt{2}}$ 
	Criamos o $Q_{21}^t = \begin{bmatrix} C & S & 0\\ -S & C& 0\\ 0& 0&1 \end{bmatrix} = \begin{bmatrix}  1/\sqrt{2} & -1/\sqrt{2} & 0\\ 1/\sqrt{2} & 1/\sqrt{2} &0\\ 0&0&1 \end{bmatrix}$ 
	$\displaystyle Q_{21}^tA=\begin{bmatrix}  1/\sqrt{2} & -1/\sqrt{2} & 0\\ 1/\sqrt{2} & 1/\sqrt{2} &0\\ 0&0&1 \end{bmatrix}\begin{bmatrix} 1 & 2 &4\\ -1& 2& 1\\ 1 & -1& 3\end{bmatrix}=\begin{bmatrix}\sqrt{2} & 0 &3/\sqrt{2}\\0 & 4/\sqrt{2} & 5/\sqrt{2}\\ 1&-1&3\end{bmatrix}$ 
	**Encontramos outra matriz para anular o $a_{31}$**
	$Q_{31}^t = \begin{bmatrix} C&0&S\\0&1&0\\-S&0&C\end{bmatrix} = \begin{bmatrix} \sqrt{2}/\sqrt{3}&0&1/\sqrt{3}\\0&1&0\\-1/\sqrt{3}&0&\sqrt{2}/\sqrt{3} \end{bmatrix}$	$k_{11} = \sqrt{\sqrt{2}^2 +1^2} = \sqrt{3}$
	$\displaystyle cos(\theta)=\frac{\sqrt{2}}{\sqrt{3}};~~sen(\theta)=\frac{1}{\sqrt{3}}=\frac{\sqrt{3}}{3}$
	fazemos
	$Q_{31}^tQ_{21}^tA = \begin{bmatrix} \sqrt{2}/\sqrt{3}&0&1/\sqrt{3}\\0&1&0\\-1/\sqrt{3}&0&\sqrt{2}/\sqrt{3} \end{bmatrix}\begin{bmatrix}\sqrt{2} & 0 &3/\sqrt{2}\\0 & 4/\sqrt{2} & 5/\sqrt{2}\\ 1&-1&3\end{bmatrix}= \begin{bmatrix}3/\sqrt{3} &-1/\sqrt{3}&6/\sqrt{3}\\0&4/\sqrt{2}&5/\sqrt{2}\\0&\frac{-\sqrt{2}}{\sqrt{3}}&3/\sqrt{6} \end{bmatrix}$
	 **Encontramos outra matriz  para anular o $a_{32}$**
	 $k_{11} = \sqrt{(4/\sqrt{2})^2 +(-\sqrt{2}/\sqrt{3})^2}= \frac{\sqrt{26}}{\sqrt{3}}$ 
	  
		 $cos(\theta)=(4/\sqrt{2})/(\sqrt{26}/\sqrt{3})= 2\sqrt{3}/\sqrt{13};~~sen(\theta)=-\sqrt{3}/\sqrt{26}$
	 $Q_{32}^t = \begin{bmatrix} 1&0&0\\ 0&C&S\\0&-S&C\end{bmatrix}=\begin{bmatrix} 1&0&0\\ 0&2\sqrt{3}/\sqrt{13}&-\sqrt{3}/\sqrt{26}\\0&\sqrt{3}/\sqrt{26}&2\sqrt{3}/\sqrt{13}\end{bmatrix}$ 
	 fazemos $Q_{32}^tQ_{31}^tQ_{21}^tA=\begin{bmatrix} 1&0&0\\ 0&2\sqrt{3}/\sqrt{13}&-\sqrt{3}/\sqrt{26}\\0&\sqrt{3}/\sqrt{26}&2\sqrt{3}/\sqrt{13}\end{bmatrix}\begin{bmatrix}3/\sqrt{3} &-1/\sqrt{3}&6/\sqrt{3}\\0&4/\sqrt{2}&5/\sqrt{2}\\0&-1&3/\sqrt{6} \end{bmatrix}$ =$\begin{bmatrix} 3/\sqrt{3} &-1/\sqrt{3}&6/\sqrt{3}\\ 0&\frac{\sqrt{3}-2\sqrt{2}}{3\sqrt{3}}&\frac{10\sqrt{6}-3}{3\sqrt{3}}\\ 0&0&\frac{5\sqrt{3}+6\sqrt{2}}{3\sqrt{6}}\end{bmatrix}$
	 

## Usando [[Transformação de Householder]]
**Caso exemplar**

$A = \begin{bmatrix} 1&2&-4\\2&6&7\\-2&1&8\end{bmatrix}$, objetivo é encontrar a QR.
Lembrete: $QA = (I-\gamma uu^t)A = A-\gamma u (u^t a)$, com $\displaystyle \gamma = \frac{2}{\|u\|^2}$, $u=A_n + sig(A_n[1]).\|A_n\|$  

1° Etapa: $Q_1A_1= Q_1\begin{pmatrix}1\\2\\-2\end{pmatrix}$ , onde $A_1$ é a primeira coluna
$sig(A_1[1]).\|A_1\|= 1.\sqrt{1^2+2^2+(-2)^2}=\sqrt{9}=3$
$u_1 = \begin{pmatrix}1\\2\\-2\end{pmatrix}+\begin{pmatrix}3\\0\\0\end{pmatrix}= \begin{pmatrix}4\\2\\-2\end{pmatrix}$, $\displaystyle \gamma = \frac{2}{\sqrt{4^2+2^2+(-2)^2}}= \frac{1}{12}$ 
$\displaystyle I-\frac{1}{12}\begin{pmatrix}4\\0\\-2\end{pmatrix}\begin{pmatrix}4&0&-2\end{pmatrix}\begin{pmatrix}1\\2\\-2\end{pmatrix}= \begin{pmatrix}1\\2\\-2\end{pmatrix}-\frac{1}{12}12\begin{pmatrix}4\\2\\-2\end{pmatrix}= \begin{pmatrix}-3\\0\\0\end{pmatrix}$

$\displaystyle I -\frac{1}{12}\begin{pmatrix}4\\0\\-2\end{pmatrix}\begin{pmatrix}4&0&-2\end{pmatrix}\begin{pmatrix}2\\6\\1\end{pmatrix} = \begin{pmatrix}-4\\3\\4\end{pmatrix}$
$\displaystyle I-\frac{1}{12}\begin{pmatrix}4\\0\\-2\end{pmatrix}\begin{pmatrix}4&0&-2\end{pmatrix}\begin{pmatrix}-4\\7\\8\end{pmatrix}=\begin{pmatrix}2\\10\\5\end{pmatrix}$
Com isso conseguimos criar uma matriz com as novas colunas
$\begin{pmatrix}-3&-4&2\\0&3&10\\0&4&5\end{pmatrix}$, perceba que essa é a equivalente a $Q_1$ do método anterior

2° Etapa
$\sqrt{3^2+4^2}=5$
$u = \begin{pmatrix}3\\4\end{pmatrix}+\begin{pmatrix}5\\0\end{pmatrix}= \begin{pmatrix}8\\4\end{pmatrix}$, $\displaystyle \gamma = \frac{2}{\sqrt{8^2+4^2}}= \frac{1}{40}$ 

$\displaystyle I-\frac{1}{40}\begin{pmatrix}8\\4\end{pmatrix}\begin{pmatrix}8&4\end{pmatrix}. \begin{pmatrix}3\\4\end{pmatrix}= \begin{pmatrix}-5\\0\end{pmatrix}$ 
$\displaystyle I-\frac{1}{40}\begin{pmatrix}8\\4\end{pmatrix}\begin{pmatrix}8&4\end{pmatrix}\begin{pmatrix}10&5\end{pmatrix}=\begin{pmatrix}-10\\-5\end{pmatrix}$ 

Agora
$R = \begin{pmatrix}-3&-4&2\\0&-5&-10\\0&0&-5\end{pmatrix}$, assim obtemos a matriz r

Supondo que $b=\begin{pmatrix}-5\\3\\5\end{pmatrix}$
$Q_1b = \left[I-\frac{1}{12}\begin{pmatrix}4\\2\\-3\end{pmatrix}\begin{pmatrix}4&2&-2\end{pmatrix}\right]\begin{pmatrix}-5\\3\\5\end{pmatrix}=\begin{pmatrix}3\\7\\1\end{pmatrix}$
$Q_2Q_1b = \left[I-40\begin{pmatrix}8\\4\end{pmatrix}\begin{pmatrix}8&4\end{pmatrix}\right]\begin{pmatrix}7\\1\end{pmatrix}= \begin{pmatrix}3\\-5\\-5\end{pmatrix}$
**Pseudo-Código**
A <- Matriz que iremos decompor
Q <- Matriz que armazenaremos
R <- Matriz que armazenamos

**Para** i de 1 até colunas(A)-1
	**if** i!= 1
		**Para** j de 1 até i-1
			A[j: , i] -= 2/(norm(aux[j:, j])^2).aux[j:, j].aux[j: ,j]$^t$.A[j:, i]
			Q[j: ,i] -= 2/(norm(aux[j:, j])^2).aux[j:, j].aux[j: ,j]$^t$.Q[j:, i] 
	x = A[i: ,i]
	sigma = -sinal(x[1]).norma(x)
	x[1] -= sigma
	aux[i: ,i] = x
	A[i: ,i] -= 2/(norm(aux[i:, i])^2).aux[i:, i].aux[i: ,i]$^t$.A[i:, i] 
	Q[i: ,i] -= 2/(norm(aux[i:, i])^2).aux[i:, i].aux[i: ,i]$^t$.Q[i:, i] 
**Para** j de 1 até colunas(A)-1
	A[j: , i] -= 2/(norm(aux[j:, j])^2).aux[j:, j].aux[j: ,j]$^t$.A[j:, i]
	Q[j: ,i] -= 2/(norm(aux[j:, j])^2).aux[j:, j].aux[j: ,j]$^t$.Q[j:, i] 
**if** (Linhas(A) > Colunas(A))
	m <- coluna(A)
	n <- linha(A)
	x = A[m: , m]
	sigma = -sinal(x[1]).norma(x)
	x[1] -= sigma
	aux[m:, m)]
	A[m: , m] -= 2/(norm(aux[m:, m])²).aux[m:, m].aux[m: ,m]$^t$.A[m:, m]
	Q[m: ,m] -= 2/(norm(aux[m:, m])²).aux[m:, m].aux[m: ,m]$^t$.Q[m:, m] 
**Complexidade do algoritmo**
	
```julia
using LinearAlgebra
function Householder(A)
  #= A::array é a matrix que queremos a r e ela tem posto cheio
    
  Return: Retorna a matriz R triangular superior e a função Q que rotaciona o sistema
=#

  n,m = size(A); #Obtemos a quantidade de linhas e colunas
  if (n < m) # Verifica posto
    error("A matriz não tem posto cheio")
  end

  sigma = zeros(m); #Armazenar os valores de sigma
  Q = Matrix{Float64}(I,n,n); # Aqui iremos salvar as transformações
  aux = zeros(n,m); # Aqui iremos salvar os u

  for i in 1:m-1 # Percore as m-1 colunas
    if (i != 1)
      #Zeramos a linha da matriz A
      for j in 1:i-1
         A[j:end, i] = A[j:end, i] - (2/(norm(aux[j:end, j])^2))*aux[j:end, j]*aux[j:end, j]'*A[j:end, i]
         Q[j:end, i] = Q[j:end, i] - (2/(norm(aux[j:end, j])^2))*aux[j:end, j]*aux[j:end, j]'*Q[j:end, i]
      end 
    end

    x = A[i:end, i];
    sigma[i] = -sign(x[1])*norm(x);

    x[1] = x[1]-sigma[i];
    aux[i:end, i] = x;

    A[i:end, i] = A[i:end, i] - (2/(norm(aux[i:end, i])^2))*aux[i:end, i]*aux[i:end, i]'*A[i:end, i]
    Q[i:end, i] = Q[i:end, i] - (2/(norm(aux[i:end, i])^2))*aux[i:end, i]*aux[i:end, i]'*Q[i:end, i]

  end

  #Rotacionamos a ultima coluna
  for j in 1:m-1
    A[j:end, m] = A[j:end, m] - (2/(norm(aux[j:end, j])^2))*aux[j:end, j]*aux[j:end, j]'*A[j:end, m]
    Q[j:end, m] = Q[j:end, m] - (2/(norm(aux[j:end, j])^2))*aux[j:end, j]*aux[j:end, j]'*Q[j:end, m]
  end 

  if (n > m) # Temos que zerar as linhas a mais
    x = A[m:end, m];
    sigma[m] = -sign(x[1])*norm(x);

    x[1] = x[1]-sigma[m];
    aux[m:end, m] = x;
    A[m:end, m] = A[m:end, m] - (2/(norm(aux[m:end, m])^2))*aux[m:end, m]*aux[m:end, m]'*A[m:end, m];
    Q[m:end, m] = Q[m:end, m] - (2/(norm(aux[m:end, m])^2))*aux[m:end, m]*aux[m:end, m]'*Q[m:end, m];
  end

return Q, A;

end
```

