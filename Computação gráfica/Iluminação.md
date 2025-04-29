- Converter objetos gráficos em imagens


### Modelo ABD
- Ambiente
	- Iluminação de uma fonte contínua a todos os objetos, exemplo: sol, lâmpada etc
	- Na prática é a cor que o objeto irá mostrar
	- $I_{ambiente}=light_{ambiente}*material_{ambiente}$

- Difusa
	- Temos que pode iluminar um ambiente, mas ela tem uma boa definição de origem e onde ilumina
	- $I_{difusa}=light_{difusa}*material_{difusa}*\cos(\theta) = light_{difusa}*material_{difusa}*\max((\hat n . \hat l), 0)$
	
- Especular
	- Fonte intensa que permite calcular a replexão
	- $I_{especular}=light_{especular}*material_{especular}*\max((\hat r .\hat v)^n, 0)$
	- n é o **brilho**
	

$$I_{\text{observador}}=I_{ambiente}+I_{difusa}+I_{especular}$$
- Os valores são [[Vetor]]es, então a soma é vetorial

- abrir o coelho