**Formatação em C**

Inteiro (```"%d" ```)
Ponteiro (```"%p"```)

## Desvio e repetição
- **If**
	```c
	if (expressão lógica){
		Bloco de comandos
	}```

	**Composto**
	```c
	if(expressão lógica){
		Bloco de comandos
	} else{
	}```
- Switch
```c
switch(Variável){
	case conteúdo:
	bloco de comandos
	break;
	
	case conteúdo2:
	...

	case conteúdo n:
	default:
		conteúdo
		break;
}
```
- goto
- break - Continue
- while
- for, do while

	Do while execulta uma vez e a partir dessa execulção ele começa a rodar o for
	```c
	do {bloco de comando}
	while(expressão lógica)
	```

## Operadores lógicos
```&&``` Operador de e
```||``` Operador de ou
```!``` Operador de Negação