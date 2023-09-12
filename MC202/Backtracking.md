- é uma estratégia para resolver problemas computacionais por busca exaustiva, que baseada em restrições é capaz de eliminar muitas soluções
- Usado para encontrar [[Caminho Hamiltoniano]]



**Pseudo-algoritmo**
	função Backtrack()
```c
bool Backtrack(<solução candidata>){
	<variável local>
	if (<solução encontrada>){
		<Processa a solução>}
	else{
		<gera uma lista de candidatas que satisfazem as restrições>
		<execulta Backtrack para cada solução candidata>}
	return (<True/False>)
}
	```

