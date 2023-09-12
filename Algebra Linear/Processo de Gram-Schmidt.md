consiste em um processo iterativo para encontrar uma base ortogonal

- Supomos que R³ tem bases ortonormais $u_1,~ u_2 ~ e~ u_3$
- por ser ortonormal, o [[Produto interno]] entre os elementos é 0

Normalizamos os vetores e obtemos $v_1 = \frac{u_1}{||u_1||}$, $v_2 = \frac{u_2}{||u_2||}$ e $v_3 = \frac{u_3}{||u_3||}$ 

Se procurarmos o vetor de S mais parecido com um ponto b fora do conjunto,temos$$\displaystyle \large k = min_{x\in S}||x_1v_1 + x_2v_2+...+x_nv_n-b||^2$$
#### Algoritmo
- Dado um conjunto de vetores $u_1,~u_2,^...,u_n$ . Normalize cada um, criando assim $v_1,~v_2,~...,v_n$ | cada $||v_i|| =1$ 
	Tome $u_1$ como o primeira base do sistema

	Para cada vetor $v_i$:
		$base^{(i)}$ <-- $\displaystyle v_i- \sum_{k=1}^{i-1} \frac{<v_i,v_k>}{1}\vec v_k$ ; para k>1

#### Octave
```octave
function M = gram(M)
% M é uma matriz em que os vetores são linha coluna

[lin, colun] = size(M); # Dimensões de M
B = zeros(lin,colun); # Vetor com o resultado

a = sqrt(sum(M(:,1)));
M(:,1) = M(:,1)/a; #Normaliza a coluna 1
display(M)
B(:,1) = M(:,1); # Consideramos o primeiro como uma base
for i = 2:colun # encontramos as bases para 
	v = M(:,i);
	for k =1:i-1 # todos os vetores já normalizados
		v -= dot(M(:,i),M(:,k))*M(:,k);
	endfor	
	M(:,i) = v/sqrt(dot(v,v)); # normaliza
endfor
endfunction
```
#### Julia
```julia
function gram(M)

#  M é uma matriz em que os vetores são linha coluna
# M precisa ser uma matriz de número float ou number
lin, colun = size(M); # Dimensões de M
B = zeros(Number, lin, colun); # Vetor com o resultado
a = Number(sqrt(sum(M[:,1])));
M[:,1] = M[:,1]/a;  #Normaliza a coluna 1
B[:,1] = M[:,1]; # Consideramos o primeiro como uma base
for i = 2:colun # encontramos as bases para 
	v = M[:,i];
	for k =1:i-1 # todos os vetores já normalizados
		v -= sum(M[:,i]*M[:,k]')*M[:,k];
	end	
	M[:,i] = v/sqrt(sum(v'*v)); # normaliza
end
return M
end
```