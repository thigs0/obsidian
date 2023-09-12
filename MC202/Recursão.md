- Similar ao processo de [[Complementos de matemática/Indução]] matemática


****
**Escrever um código para inverter uma lista simples**
![[recursão_inverte.canvas]]
```c
void Inverte(Lista **ini, NoLista *ant){
	// init é um endereço do endereço do primeiro elemento
	//
	
	if (*ini != NULL){ // Caso a lista não esteja vazia
		if (*ini)->prox = NULL{
			(*ini)->prox = ant;
		}else{
			Lista *PaiAnt = ant;
			ant = *ini; ini = (*ini)-prox;
			ant -> prox = PaiAnt;}
	}
}
```

****
