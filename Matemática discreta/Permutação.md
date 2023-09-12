otivação: Dados n objetos, quantas permutações consigo formar com estes objetos
- Prova da fórmula geral por [[Complementos de matemática/Indução]]. n!
Para n=1, temos apenas uma permutação; 1!=1. Portanto é válida quando n=1.
Suponha que é válida para um dado n. Tome $A=\{a_1,a_2,...,a_{n+1}\}$ 


**[[Permutação caótica]]**
- É uma permutação em que nenhum elemento está na i-ésima posição
- Isso é, a letra não volta para a posição em que estava na palavra que quer ser permutada

**Exemplo**
dessaranjo da palavra amor
| amor |      |      |
| ---- | ---- | ---- |
| maro | mora | mrao |
| oarm | oram | orma |
| ramo | roam | roma     |

O que pode ser visto pelo exemplo de [[Recursão]]
![[mindmap_permutacao_caotica]]
A quantidade é dada por [[Subfatorial]]

A soma infinita é
$$!n = \frac{1}{n!}\sum_{k=0}^n \frac{(-1)^i}{i!};~~~\forall n\geq 0$$

$\displaystyle !n = \left[ \frac{n!}{e}\right]$ em que [] Representa o inteiro próximo do valor interno
que no exemplo acima seria
$\displaystyle \frac{4!}{e}= [8,829106588] =9$ 
