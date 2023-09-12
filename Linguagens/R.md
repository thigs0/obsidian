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