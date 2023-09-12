- Armazenar uma sequência sem a necessidade de um limite superior
- Os elementos podem estar distribuídos de qualquer maneira na memória interna do computador
- Normalmente é implementada em em [[C]]
- **Lista ligada simples**
	é uma sequência de elementos, onde a  inserção e a remoção de um elemento pode ocorrer em qualquer ponto da sequência
	- O último elemento aposta para o `NULL`
```c
typedef struct _no_lista{
	int info;
	struct nolista *prox;
	}ListaSimples;

int *CriaLista(){
	ListaSimples p;
	p->nolista = NULL;
	p->_No
	return (&ListaSimples);
}

void PushEnd(ListaSimples *Vector, int v){
	//percorre a lista até encontrar o valor null
	* prox = Vector->nolista;
	while (prox != NULL){
		prox = *(Vector->prox);
	}
	// cria o elemento que será o último
	ListaSimples t;
	t.info  = v;
	*prox = t;
}

int *SearchNum(){
	
}

```
