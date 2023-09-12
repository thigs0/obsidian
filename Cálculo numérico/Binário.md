- ### Algoritmo
	Pseudo-Algoritmo
		$\displaystyle r_1 = r; k=1$
		Enquanto $r_{k+1} for ~~diferente~~ de~~ 0$
			Se a divisão inteira de $r_k$ = 1
				$d_k$ é 1
			Se a divisão inteira de $r_k$ = 0
				$d_k$ é 0
			k = k + 1
		

```python

def DecimalToBinario(number):  
    k=number  
    temp = ''  
    while k != 0:   
        if k % 2 == 1: # caso a divisão não seja inteira  
            temp += '1'  
            k = int(k/2)  
        else:  
            temp += '0'  
            k /= 2  
    return temp[::-1]

def BinarioToDecimal(number):
	k = str(number)[::-1] 
	cont=temp=0
	for i in k:
		temp += int(i)*2**(cont)
		cont+=1
	return temp
	
```

```julia
function DecimalToBinario(number)
	int(x) = trunc(Int,x)
	k = number
	temp = ""
	while k != 0
		if k % 2 == 1 # caso a divisão não seja inteira
			temp *= "1";
			k = int(k/2);
		else
			temp *= "0";
			k = int(k/2);
		end
	end
return reverse(temp)
end

function BinarioToDecimal(number)
	k = reverse(string(number));
	temp = 0
	cont =0
	for i in k
		temp += parse(Int64,i)*2^(cont)
		cont+=1
	end
	return temp
end
```
