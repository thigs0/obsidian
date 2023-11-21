é um jogo em que temos três astes e inicialmente uma delas tem $n$ círculos formando uma torre. O objetivo é mover a torre para a aste lateral usando a central e sem que uma peça grande fique em cima de uma pequena
![[300px-Tower_of_Hanoi.jpeg|400]]

Verificando a quantidade mínima de passos para resolver o jogo usando [[Relação de recorrencia]] 
Temos que $T_n$ é a quantidade de movimentos para mover uma torre de n discos da esquerda para direita
movemos (n-1) discos para a direita duas vezes e resta apenas um disco para completarmos o jogo, então
$$T_n=2T_{n-1}+1$$
$$T_n+1=2(T_{n-1}+1)\Rightarrow \tau_{n}=2\tau_{n-1}$$ que é uma progressão geométrica de razão 2, $\tau_{n}= 2^n$
$$T_n+1=2\tau_{n-1}\Rightarrow T_n=2.2^{n-1}-1\Rightarrow \boxed{T_n =2^n-1}$$
Resolvendo a equação não-homogênea