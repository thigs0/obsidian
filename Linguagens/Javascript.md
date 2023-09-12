- Para mostrar algo na tela como um pop-up temos os comandos
```Js
window.alert('Minha primeira mensagem'); // cria uma mensagem pop-up

window.confirm('Está gostando de javascrip?') // Cria um pop-up com opção cencelar e ok

a = window.prompt('Qual o seu nome?') // Cria um pop um com uma caixa de texto
```

- Comentários em javascrip
```Js
// Comentário de linha única

/*
Comentário múlti linha
*/
```

- Criar uma variável
```Js
var nome ='Thiago Santos da Silva' // pode aspas simples
var nome ="Thiago Santos da Silva"// ou aspas duplas
```

- Varificar o tipo da variável
```Js
var n =200
typeof n // irá mostrar 'number'
```

- Conversão
```Js
var n = '1.1'

	// De String para numero
var n = Number.parseInt(n)
var n = Number.parseFloat(n)
var n - Number(n)

	// De number para string
var n = String(n)
var m = n.toString()
```

- Escrevendo na tela
```Js
var aluno = 'Thiago'
var idade = 18
var nota = 9.1

`O aluno ${aluno} que tem ${idade}, tirou ${nota}` // Usamos crase para formatar um texto deste modo

```

- Comandos
```Js
var aluno = 'Thiago'
aluno.length // Retorna o tamanho da string
aluno.toUpperCase() // Coloca a escrita em maiusculo
aluno.toLowerCase() // Coloca a escrita em minusculo

document.write(``) // Escreve no documento

var n = 10
n.toFixed(2) // força 2 casas decimais
n.toLocaleString("pt-BR",{style: 'currency', currency:"BRL"})
n1.replace('.', ',') // Substitui ponto por virgula
```

- Atribuição
```Js

n += 5 //o valor recebe ele mais 5
n -= 5 //o valor recebe ele menos 5
n *= 5 //o valor recebe ele vezes 5
n **= 5 //o valor recebe ele elevado a 5
n /= 5 //o valor recebe ele dividido por 5
n++ // soma um no n
n-- // subtrai um do n 
```

- Operadore
```Js

! // significa não
&& // é o conjunção (e)
|| //é o disjunção (ou)

? : //Teste lógico ? ação de True: ação do false
```

Evento
```Js

# Criar uma função
function nome_da_função(/param/ ){
	/Nesta parte vêm o código da função
		}
```

# Condições

```js
if (Condição){
Bloco 1
} else {
Bloco 2
}
```


```Js
console.log('O console funcionou corretamente') // mostra algo na tela no Nodejs

var vel = 60.5 // velocidade de um carro
console.log(`A velocidade de seu carro é ${vel} Km/h`)
if (vel >60){
	console.log(`Você ultrapassou a velocidade permitida. Multado`)
}
console.log(`Dirija com segurança`)
```

- **Condição múltipla**
```Js
var dia = new Date()

var dia = dia.getDay() // Usa uma bliblioteca para achar o dia da semana

console.log(dia)

switch(dia){

case 0:

console.log('Domingo')

break
 

case 1:

console.log("Segunda")

break

  
case 2:

console.log("Terça")

break

  
case 3:

console.log("Quarta")

break

  
case 4:

console.log("Quinta")

break

  
case 5:

console.log("Sexta")

break

  
case 6:

console.log("Sabado")

break

}
```