- Algoritmo do tipo dividir para conquistar
![MergeSort_gif](https://upload.wikimedia.org/wikipedia/commons/c/c5/Merge_sort_animation2.gif)
- Usa [[Recursão]] para dividir o problema em dois menores e resolver eles, pode não ser muito eficiente em certos casos

**Pseudo-código**
```
função mergesort (vetor a)
     se (n == 1) retornar a

     vetor l1 = a[0] ... a[n/2]
     vetor l2 = a[n/2 + 1] ... a[n]

     l1 = mergesort(l1)
     l2 = mergesort(l2)

     retornar mesclar(l1, l2)
fim da função mergesort

função mesclar (vetor a, vetor b)
     vetor c

     enquanto (a e b têm elementos)
          if (a[0] > b[0])
               adicionar b[0] ao final de c
               remover b[0] de b
          senão
               adicionar a[0] ao final de c
               remover a[0] de a
     enquanto (a tem elementos)
          adicionar a[0] ao final de c
          remover a[0] de a
     enquanto (b tem elementos)
          adicionar b[0] ao final de c
          remover b[0] de b
     retornar c
fim da função mesclar
```
