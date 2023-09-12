Consiste em tomar o seguinte [[Limite]]:
$$\lim_{t \to 0} \frac{f(a+t)-f(a)}{t}$$
- ### Derivadas notáveis
	 $\displaystyle \Large \frac{d}{dt}\sin(x) = \cos(x)$ 
		 **Demonstração**:
		 $\displaystyle \frac{d}{dt} \sin(x) = \lim_{t \to 0} \frac{\sin(x+t)-\sin(x)}{t}$, usamos a relação  
		 " $\sin(a)-\sin(b) = 2\sin(\frac{a-b}{2})\cos(\frac{a+b}{2})$ "
			=> $\displaystyle \lim_{t \to 0} \frac{2sin(\displaystyle\frac{x+t-x}{2}).\cos(\displaystyle\frac{x+t+x}{2})}{t}$ 
			$\displaystyle \lim_{t \to 0} \frac{2\sin(\frac{t}{2})\cos(\frac{2x+t}{2})}{t} = \lim_{t \to 0} \frac{2\sin(\frac{t}{2})\cos(x+\frac{t}{2})}{t}$  Cosseno soma
			$\displaystyle \lim_{t \to 0} \frac{2 \sin(\frac{t}{2})[\cos(x)\cos(\frac{t}{2})-\sin(x)\sin(\frac{t}{2})]}{t}$ Colocamos o 2 como divisor
			$\displaystyle \lim_{t \to 0} \frac{\sin(\frac{t}{2})[\cos(x)\cos(\frac{t}{2})-\sin(x)\sin(\frac{t}{2})]}{\frac{t}{2}}$
			$\displaystyle \lim_{t \to 0} \frac{\cos(x)\cos(\frac{t}{2})\sin(\frac{t}{2})-\sin(x)\sin(\frac{t}{2})\sin(\frac{t}{2})}{\frac{t}{2}}$, usamos [[Limite da soma]]
			$\displaystyle \lim_{t \to 0} \frac{\cos(x)\cos(\frac{t}{2})\sin(\frac{t}{2})}{\frac{t}{2}}- \lim_{t \to 0} \frac{\sin(x)\sin(\frac{t}{2})\sin(\frac{t}{2})}{\frac{t}{2}}$, usamos [[Limite do produto]]
			$\displaystyle \lim_{t \to 0} cos(x).\lim_{t \to 0}\cos\left(\frac{t}{2}\right).\lim_{t \to 0} \frac{\sin\left(\frac{t}{2}\right)}{\frac{t}{2}}- \lim_{t \to 0} \sin(x).\lim_{t \to 0} \sin\left(\frac{t}{2}\right).\lim_{t \to 0} \frac{\sin\left(\frac{t}{2}\right)}{\frac{t}{2}}$
			usamos o [[Limite fundamental da trigonometria]]					=> $= \displaystyle \lim_{t \to 0} \cos(x).\lim_{t \to 0} \cos\left(\frac{t}{2}\right)-\lim_{t \to 0} \sin\left(x\right).\lim_{t \to 0} \sin\left(\frac{t}{2}\right)$ 	
			e sabendo que 
			$\displaystyle \begin{cases} \displaystyle\lim_{t \to 0} \cos(x) = cos(x)\\ \lim_{t \to 0} \cos\left(\frac{t}{2}\right)= 1 \\ \lim_{t \to 0} \sin\left(\frac{t}{2}\right)= 0\\ \lim_{t \to 0} \sin(x) = \sin(x)\end{cases}$
			=>$\displaystyle \Large \frac{d}{dt} \sin(x) = cos(x)$ 
	$\displaystyle \Large \frac{d}{dt}\cos(x) = -\sin(x)$
		**Demonstração**:
		$\displaystyle \frac{d \cos(x)}{dx}=\lim_{t\to 0}\frac{\cos(x+t)-\cos(t)}{t}=\lim_{t \to 0}\frac{\cos(x)\cos(t)-\sin(x)\sin(t)-\cos(x)}{t}$ 
		=> $\displaystyle \lim_{t \to 0}\frac{\cos(x)[\cos(t)-1]-\sin(x)\sin(t)}{t}= \lim_{t \to 0}\frac{\cos(x)[\cos(t)-1]}{t}-\lim_{t \to 0}\frac{\sin(x)\sin(t)}{t}$ Assim, no segundo termo temos o [[Limite fundamental da trigonometria]] e no primeiro temos que realizar uma mudança de função por $-2\sin^2(t/2)=\cos(t)-1$
		De modo, que obteremos novamente o limite fundamental e um termo de seno, que tende à 0. Restando apenas o seno de x...
		$\displaystyle \frac{d\cos(x)}{dx}=-\sin(x)$ 
	$\displaystyle \Large \frac{d}{dt}\tan(x)= \frac{1}{cos^2(x)} = sec^2(x)$ 
		**Demonstração**:
		$\displaystyle \frac{d}{dx}Tg(x) = \frac{d}{dx}\left(\frac{\sin(x)}{\cos(x)}\right)= \frac{\sin'(x)\cos(x)-\sin(x)\cos'(x)}{\cos^2(x)}$
		$\displaystyle = \frac{\cos^2(x)+\sin^2(x)}{\cos^2(x)}=\frac{1}{\cos^2(x)}=\sec^2(x)$ 
	
	$\displaystyle \Large \frac{d}{dx}f^{-1}(x) = \frac{1}{f'(f^{-1}(x))}$ 
		**Demonstração**
		Sabemos que $f(f^{-1}(x))=x$ e assim, aplicamos a [[Regra da cadeia]]
		$\displaystyle f'(f^{-1}(x))\frac{d}{dx}f^{-1}(x)=1$ => $\displaystyle \frac{d}{dx}f^{-1}(x) = \frac{1}{f'(f^{-1}(x))}$
	$\displaystyle \Large \frac{d}{dt} ln(x)= \frac{1}{x}$ 
		**Demonstração:** (Pela função inversa)
		Sabemos que $exp^{-1}(x)=\ln(x)$  e que $\frac{d}{dx}exp(x)=exp(x)$.=>
		$\displaystyle \frac{d}{dx}exp^{-1}(x) = \frac{1}{exp(\ln(x))}=\frac{1}{x}$ 
		**Demonstração:** (Pela definição)
		temos:
		$\displaystyle \frac{d}{dx}\ln(x) = \lim_{t\to 0}\frac{\ln(x+t)-\ln(x)}{t}=\lim_{t\to 0}\frac{\ln\left(\displaystyle \frac{x+t}{x}\right)}{t}=\lim_{t\to 0}\frac{1}{t}\ln\left(1+\frac{t}{x}\right)= \lim_{t\to 0}\ln\left(\left(1+\frac{t}{x}\right)^{1/t}\right)$ 

	$\displaystyle\Large \frac{d}{dx}Arctan(x)=\frac{1}{1+x^2}$ 
	$\displaystyle \Large \frac{d}{dx}Arcsin(x) \frac{1}{\sqrt{1-x^2}}$
	$\displaystyle \Large\frac{d}{dx}Arccos(x)=-\frac{1}{\sqrt{1-x^2}}$
	
 
- #### Regras de derivadas
	$\displaystyle \frac{d}{dt}\left( f+g\right)(x) = \frac{d}{dt}f(x) +\frac{d}{dt}g(x)$ 
		**Demonstração**:
		$\displaystyle (f+g)'(x) = \lim_{h\to 0}\frac{(f+g)(h+x)-(f+g)(x)}{h}$ podemos reagrupar
		$(f+g)'(x)=\lim_{h\to 0}\frac{[f(x+h)-f(x)]+[g(x+h)-g(x)]}{h}$ =>
		$(f+g)'(x)= \lim{h\to 0}\frac{f(x+h)-f(x)}{h}+\lim_{h\to 0}\frac{g(x+h)-g(x)}{h}=f'(x)+g'(x)$
	$\displaystyle \frac{d}{dt} (f.g)(x) = \frac{d f(x)}{dt}.g(x)+f(x)\frac{d g(x)}{dt}$ 
		**Demonstração**:
		$\displaystyle (f.g)(x) = \lim_{h\to 0} \frac{(f.g)(x+h)-(f.g)(x)}{h}= \lim_{h\to 0}\frac{f(x+h)g(x+h)-f(x)g(x)}{h}$
		Somamos e subtraímos f(x) de forma
		$\displaystyle = \lim_{h\to 0}\frac{[f(x+h)-f(x)+f(x)]g(x+h)-f(x)g(x)}{h}$  
		= $\lim_{h\to 0}\frac{}{}$
	$\displaystyle \frac{d}{dt}\left( \frac{f(x)}{g(x)}\right)$ = $\displaystyle \frac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2}$ 

***Teorema***
Se f é diferenciável até segunda ordem. Suponha que $f'(a)=0$, se $f''(a)>0$ então f tem um ponto de mínimo em a. Se $f''(a)<0$ então f tem um ponto de máximo local

- ### [[Teorema fundamental do cálculo]]
	Seja F uma função tal que sua $\displaystyle \frac{d}{dt}F = f$, então a [[Integral]] de f é dado pela função F mais uma constante. De modo que F é chamada de primitiva$$\int_a^b f(x)dx = F(b)-F(a)~~~~~;F'=f$$





