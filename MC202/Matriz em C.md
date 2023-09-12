- Representação de [[Matriz]] na linguagem C
```c
int * matriz(){
	int c[2];
}
```

[[C]] é um vetor de ponteiro
C = [1X00, 2X00, 3X00, 4X00]

Acessando o ponteiro 
``` *1X00 = [1, 2, 3, 4]```

### Alocar memória
```c
x = (int *)calloc(10, sizeof(int)); // Completa com 0
// ou
x = (int *)malloc(10 * sizeof(int));
```


String = ["G", "A", "B", "Y", "S"] = "GABYS"