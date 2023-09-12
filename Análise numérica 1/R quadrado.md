R-quadrado ($R^2$) é uma medida estatística da qualidade da função de encontrar uma correlação para os dados originais. Isto é, quantos dados originais a função consegue explicar.

$$R^{2}= \frac{Variação~Explicada}{Total}$$
- Sempre aumenta com a inclusão de uma dimensão a mais

---

Considere os pontos abaixo 
```y =[0.6471548437447207, 0.9204590144704543, 2.5646648163866628, 3.9408672990002986, 4.997929062762585, 4.444348392943729, 0.021112902380068244, 7.171217471120639, 6.912880731660746, 2.7570155131620586, 2.86374114521662, 6.19506580586393, 11.193661486713863, 9.285980771398757, 2.6590502734306556, 7.149863382585245, 14.05082783521062, 0.13582121938003344, 11.685427262251746, 2.9513902638908784, 17.862845683275538, 4.441014944421875, 8.842325322636277, 9.662499215766031, 19.742862390913064]```
![[dados.png|center|500]]
Calculamos o $y_{médio}$ => $\bar y =6.524001082023484$ 
Assim, para saber o erro com base na média.
$\displaystyle SQ_{tot} = \sum_{i=0}^{n} (y_i - \bar y)^{2} = 669.9942928799096$ 

E realizamos o [[Cálculo numérico/Quadrados mínimos|Quadrados mínimos]] para achar a melhor solução.
e acabamos com uma função tal que f(x) seja a função ajustadora.

Assim o erro da aproximação é $SQ_{res} = \displaystyle \sum_{i=0}^{n} (f(x_i) - \bar y)^{2} = 1889.9018168062262$
$\displaystyle SQ_{exp} = \sum_{i=0}^{n}(f(x_i)- \bar y)^{2}= 244.9756592229787$
Por fim, temos que 
$\displaystyle \large R^{2}= \frac{SQ_{exp}}{SQ_{tot}} = \frac{244.9756592229787}{669.9942928799096} = 0.3656384268140152$ 

---
#### Algoritmo
**Pseudo-Algoritmo**
y <- dados
n <- Dimensão de y

$y_{médio}$ <- Soma(y)/n
Total <- 0
Exp <- 0

**Para** i de 1 até n
	Exp += $(f(x_i)- y_{médio})^2$

**Para** i de 1 até n
	Total += $(y_i~-~y_{médio})^2$

$R^2$ = Exp/Total

**Complexidade**
$$4n => O(n)$$

```julia
function R_quadrado(x, y, f)
#= x e y são os dados plotados
=#
	n = size(y)[1];
	exp = t = 0;
	ym = sum(y)/n;

	for i in 1:n
		exp += (f(x[i])-ym)^2
	end
	for 
		t += (y[i] - ym)^2
	end
	
	return exp/t;
end
```

---
