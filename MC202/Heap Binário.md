- Estrutura baseada em [[Árvore binária]]

##### Heap max
- significa que o nó pai é sempre maior do que o nó filho
	**Construir**
	- Formar um novo nó na raiz inicial do salto
	- Dê-lhe um valor
	- Após atribuir um valor, compare os valores do nó pai e filho
	- Caso o pai seja inferior a qualquer uma das crianças, troque os nós
	- Repita a etapa até que o maior elemento atinja os nós de origem da raiz
	
	**Remover nó**
	- pegue o último nó de criança e mova-o para o último nível da raiz
	- Comparar os nós das crianças e dos pais
	- Se o valor dos pais for inferior aos nós de seus filhos, seria melhor trocá-los, seguido pela repetição do processo até satisfazer a pilha.
[[Heap min]]
- Significa que o nó pai sempre é menor do que o nó filho
	**Construir**
	- Formar um novo nó infantil no nível mais baixo, que é o fim da pilha
	- Incorporar a nova chave no nó 
	- Comece a mover a criança para cima, certificando-se de que você satisfaça por propriedade amontoada, alcançando o nó de raiz

	**Remover**
	- **Proceder simplesmente apagando o nó-raiz**
	- Mover a chave da última criança para a raiz
	- Realizar uma análise comparativa entre o nó e seus filhos
	- Se o valor dos pais for superior aos nós da criança, certifique-se de trocá-los, repetindo o processo até que você satisfaça a propriedade da pilha