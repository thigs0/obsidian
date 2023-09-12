Esta técnica particiona a sequência em relação a um pivot r ed modo que os elementos à esquerda de r sejam menores que os elementos à direita de r.

```c
void OrdenaPorParticao(int *A, int p, int q){
	int r;
	if (p<q){
	r = Particao(A, p q);
	OrdenaPorParticao(A,p,r-1);
	OrdenaPorParticao(A, r+1, q);
	}
}
```

Tempo médio é $O(nLogn)$ mas o pior caso é $O(n^2)$ 
