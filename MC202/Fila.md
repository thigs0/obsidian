 **[[Fila estática]]**

- Uma fila estática pode ser implemenntada como um [[Vetor]] de tamanho n, com os índices de início e fim

10 -> 20 -> 30 -> 40 -> .... -> n-1

- O principal ponto da fila é que o primeiro que entrou, será o primeiro a sair
Se soltarmos os elementos da fila acima, sairão na ordem
n-1, n-2, ..., 20, 10

- A implementação circular oferece maior vantagem já que os elementos na fila 
- Após inserir o novo elemento no fim, este íncide deve ser incrementado por $fim \leftarrow (fim+1)\%n$ 
- A fila está cheia se a quantidade de elementos qtde = n
- Note que quando inicio=fim pode ocorrer duas situações. Fila vazia e fila cheia, portanto é importante armazenar a quantidade de elenetos na fila
