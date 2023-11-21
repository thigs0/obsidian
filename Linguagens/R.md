Adicionar variável
```r
a <- 1 # ou
a = 1 # ou
1-> a
```

Vetor
```r
c <- c(a,b)
```

Summary(a), retorna min, mediana, max e etc dfe uma lista
library(pacote) -> Abrimos um pacote no código

& -> Uso lógico de and
| -> Uso lógico de ou 

```r
as.integer(0.15) #Converte para inteiro
round(0.98) # arredonda neste caso para 1

nomes <- c("Eduarda", "Amanda")
nomes[p] #Mostra o valor na posição p
```

### Dataframe
```r
Library(ncdf4)
Library(readr)

#Open data
df = nc_open("path")
lon <- ncvar_get("path")
dim(lon) #show the number of dimension
lat <- ncvar_get(df, "lat")
pr <- ncvar_get(df, "pr") # get variables

at = ncatr_get(df, "pr") #get units
pr.slice <- pr.array[,,1]
image(lon, lat, pr.slice) # plot map
```

**Gráficos**
*Barra vertical*
```r
barplot(table(c(
"a","a","a","a","a","b","b","b","c","c","v","v")))
```
_Barra horizontal_ 
```r
barplot(table(c(
"a","a","a","a","a","b","b","b","c","c","v","v")),
	   hor=T) #Disposição horizontal das categorias
```
_Histograma_
a função `hist()` produz um histograma dos dados informados em seu argumento
```r
x<-c(2,2,2,2,2,3,3,3,4,4,5,5,6) #vetor qualquer
hist(x)    #histograma de x
```
para facilitar a visualização, pode-se construir uma tabela
```r
table(x)
```
*plot*
```r
x <- 1:10 #Criando x
y <- c(2,5,9,6,7,8,4,1,3,10) #criando y

plot(x, y) #plota x e y

plot(x, y, #plota x e y
	xlab="Eixo x", #nomeia o eixo x
	ylab="Eixo y", #nomeia o eixo y
	main="", #título
	xlim=c(0,10), #limites eixo x
	ylim=c(0,10), #limites eixo y
	col="red", #cor dos pontos
	pch=22, #formato dos pontos
	bg="blue", #cor de preenchimento
	tcl=0.4, #tamanho de traços dos eixos
	las=1, #orientação do texto em y
	cex=1.5, #tamanho do ponto
	bty="l") #altera as bordas
```

 *plot com nomes*
 ```r
 x <- c(2,3,4,5,6,7,8,9) #Coordenadas x
 y <- c(15,46,56,15,81,11,61,55) #Coordenadas y
 nomes <- paste("cidade", LETTERS[1:8], sep="") #nomes das cidades
 cidades <- data.frame(x,y,row.names=nomes)#juntando
```