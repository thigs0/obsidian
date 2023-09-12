- Organizamos os dados de maneira a fazer com que a busca fiquem em tempo constante
- São chamados de bibliotecas etc
- São mapeadas em [[Inteiro]]s

Dado uma chave que pode ser de qualquer tipo, transformamos em um inteiro

#### Construção da função Hash
Uma forma inicial de construir uma função que transforme uma sequência de caracteres em um número inteiro, é: Somar o inteiro que representa ele na ![[Tabela ASCII]]
**Exemplo**
O nome Ulisses => 177+108+105+115+115+101+115=776
Alguns nomes e suas somas

| Nome      | Soma |
| --------- | ---- |
| danielle  | 830  |
| amanda    | 610  |
| cleópatra | 1218 |
| orlando   | 751  |
| odnalro   | 751  |
| adriana   | 720  |
| ariadna   | 720  |
Como visto, nomes que são [[Combinação]] de algum outro, têm o mesmo valor de soma. 

Para contornar esse problema, levamos em conta a posição dos caracteres
Considere um caractere no formato $C=(c_0,c_1,c_2,...c_{k-1})$
e uma sequência de as
$$c_0a^{k-1}+c_1a^{k-2}+c_2a^{k-3}+...+c_{k-2}a^1+c_{k-1}$$
Podemos tomar a como sendo um [[Número primo]], assim temos combinações de primos e tendem a ser distintos. Mas isso pode consumir muita memória. Já que os primos são infinitos.
Assim, escolhemos $i\mod(N)$, em que N é um número primo

#### Encadeamento
Caso tenhamos colisão, isto é, a função `hash` coloque dois ou mais elementos na mesma posição do vetor. Podemos ir armazenando como uma lista encadeada
0 -> 93 -> 39
1
2
3 -> 55 -> 29 -> 42
4 
5
6 -> 19
7 
8
9
10 -> 10 -> 36
12 -> 25 -> 38 -> 12

Assim, quando verificamos novamente a tabela e caímos na posição 0, precisamos comparar com 2 números, então é tempo constante

#### Método da divisão
Dado uma vetor de tamanho n.
Então pegamos a menor potência de $2^k$ tal que ele seja maior que n.
Em seguida, pegamos o menor primo mais próximo de $2^k$ 
**Exemplo**
n=200
Assim a potência de 2 mais próximo e maior é $2^8=256$ e o menor primo mais próximo é 251
Assim, a nossa função hash acaba dividindo inteiramente por 251.

Hash->lista[k]->prox