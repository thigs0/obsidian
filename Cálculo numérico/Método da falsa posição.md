
Em 1858,o escocês **A.H Rhind** (1833-1863), antiquário e advogado, adquiriu, no Egito, um papiro que continha textos matemáticos. Esse documento, que ficou conhecido como _**[Papiro_de_Rhind](https://pt.wikipedia.org/wiki/Papiro_de_Rhind "Papiro de Rhind") ou Ahmes**_ é datado do ano de 1650 a.C, e contém cerca de 85 problemas matemáticos resolvidos na forma de manual prático, copiados em escrita _hierática_, pelo escriba **Ahmes**, de um trabalho mais antigo.

Nesse papiro, esses 85 problemas se referem, na sua maioria, sobre o cotidiano dos antigos, tratando de problemas como: armazenamento de grãos, preço do pão, alimentação dos animais, etc.

Como os egípcios não tinham conhecimento da álgebra, como hoje, aplicavam técnicas aritméticas, como a **posição falsa**, e as incógnitas dos problemas eram chamadas de "_montão"_.


Dado dois pontos [a,b] de uma função contínua tais que  $$\begin{cases} f(a) >0\\ f(b) <0\end{cases}$$
**Propriedade**
1. Tem convergência garantida como o [[Método da bisseção]]
2. Pode ser mais rápido ou mais lendo que o [[Método da bisseção]]
```python
def FalsaPosicao(a,b,f,tamanho):    
    if a<0:  #Caso a não seja positivo, deixamos a>0  
      a,b = b,a    
    #Cálculamos a função nos pontos a e b  
    A = f(a)    
    B = f(b)    
    cont=0     
while abs(A) > tamanho and cont < 10**5:    
        x = (a*B - b*A)/(B-A) # cálculamos o próximo ponto      
if x> 0:    
            a = x    
        else:    
            b = x    
            cont+=1    
return a
```
```octave

```
```julia
function FalsaPosição(a,b,f,tamanho)
# deixamos a como sendo positivo
	if a <0
		a,b=b,a # troca os valores
	end
	
	A = f(a);
	B = f(b);
	cont=0
	while abs(A-B) > tamanho && cont< 10000
		x = (a*B - b*A)/(B-A); # cálculamos o próximo ponto
		if x> 0
			a =x;
		else
			b=x;
		end
		con+=1
	end
end
```