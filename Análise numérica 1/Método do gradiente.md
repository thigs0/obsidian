- Usado para minimizar funções quadráticas
- Otimizamos a quadrática $f(x) = \frac{1}{2}x^tAx-b^tx$ 

Como temos uma curva quadrática, temos um único mínimo ou máximo
- Curva quadrática em um plano
![[curve.png|center|500]]   

então quando analisamos o menos o [[Gradiente]], que é a direção para onde a função decresce mais rápido. Temos uma direção para minimizar uma função.
![[curve2.png|center|500]]

Agora, observamos que mesmo que tenhamos a melhor direção que é dada por $-\nabla f$, ainda não sabemos o quando andar; o que pode resultar em passarmos do ponto que queremos ou andarmos pouco.

Pegando o $arg~min~f(x+t d)$ 
isso equivale à $\displaystyle \frac{d}{dt}\frac{1}{2}x^tAx-b^tx=\frac{d}{dt}\frac{1}{2}(x+\alpha d) A(x+\alpha d) -b^t (x+\alpha d)=0$  

Pela [[Regra do produto]]
=> $\displaystyle \alpha [\frac{1}{2}d^{t}Ad + \frac{1}{2}d^tAd] = -\frac{1}{2}d^tA-\frac{1}{2}x^tAd+b^td$, 
=> $\alpha[d^tAd]=(b-x^tA)d$
=> $\displaystyle \alpha =\frac{(b-x^tA)}{d^tAd} = \frac{d^td}{d^tAd}$  

Agora temos a direção que é dada $-\nabla f$, e de direção $\displaystyle \alpha =\frac{(b-x^tA)}{d^tAd}$ 

---
**Pseudo código**

Dado $x_0 \in \mathbb{R}^n$ 
**Para** k=0,1,2,...
	$d_k=b-Ax_k$ 
	**Se** $d^t_{k}d_k=0$ 
		***Para***
	**Else**
		$\displaystyle \alpha = \frac{d_k^td_k}{d_kAd_k}$
	$x_{k+1}=x_k+\alpha_kd_k$   

```julia
function Gradiente(A, b, grad, x0)
	alpha = 
end
```

---
**Teorema**
$x^tx$ é [[Definida semipositiva]] e que se as colunas de x forem [[Linear independente]] então $x^tx$ é definida positiva. Portanto, existem solução $\hat \beta= (x^tx)^{-1}x^t\beta$ 
	Prova:
