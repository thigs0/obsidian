- rápido para computação científica, constroi [[Geometria Analítica/Matriz]]

```julia
println("I'm learning Julia") # Print a function
typeof(42) # Return type of variable

#=
Multicomentário
=#
```


```julia
if condição
 faz
elseif
 faz
else
 faz
end




#Método simplificado
a ? b : c # Significa

if a
	b
else 
	c
end
```

- comparação
```julia
	a && b # é o operador de and
	#Execulta b apenas se a for verdade
	
```

## Functions
```julia
function DoSomething(params)
	params+1
end

#ou

function(param) = action


# 
v = [1 2 3 4 5]
sort(v) # organiza o vetor v e retorna outro igual, mas organizado
sort!(v) # organiza o vetor v e retorna ele organizado

v.*v # igual no octave, '.' simboliza fazer a ação com cada elemento
```

- importar package
```julia
using pack
pack.add(do) # igual ao python para chamar função
```

```julia
# Dicionário
	Info = Dict("Thiago"=> "(19)99473-3371", "Gostbuster"=>"(12)98655-6561")
	Info["Thiago"] # mostra o valor para Thiago
	
	pop!(Info, "Thiago") # Retorna o valor e o remove também

#Tuple
	MyAnimal = ("Dog","cat","Turtle", "Pinguin")
	myAnimal[1] #Mostra o valor por índice

#Array
	MyFavorityAnimals = ["Dog", "bird","Horse","Arrara"]
	MyFavorityAnimals[3] # Array pega por índice
	push!(MyFavorityAnimals , "hat") # Irá adicionar "hat nop array
	
	rand(n,m) # Cria uma matriz de n linha e m colunas
	
```
```julia
while condicion

função a repetir loop
end # Finaliza o loop


for var in vector

função a repetir loop

end

# Existe o doble for loop
for var in vector, var2 in vector2
função repetir
end
```
```julia
methods(+) 

# In julia exist 180 methods for generic function
# with float and complex numbers 

#Examples
@which 3+3 # Return integer
```
