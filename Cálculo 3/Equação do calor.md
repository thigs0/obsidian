É dada pela equação
$$\Large u_t = ku_{xx}$$
E sempre supomos que 
- A seção trsnsversal é bem menor que o comprimento da barra
- As extremidades têm o mesmo valor e são conhecidos

### Resolução por separação
Podemos imaginar que a solução seja da forma $u_(x,t) = X(x).T(t)$
dessa forma temos o sistema
$\begin{cases} u(x,t) = X(x)T(t)\\ u_x(x,t) = X'(x)T(t)\\ u_{xx}(x, t) = X''(x)T(t)\\ u_t(x,t) = X(x)T'(t) \end{cases}$
Substituindo na equação obtemos 
$\displaystyle X(x)T'(t) = k (X''(x)T(t)) \Rightarrow \frac{X''(x)}{X(x)} = k\frac{T'(t)}{T(t)}$ Como as duas equação podem variar livremente sem alterar uma a outra. Então são iguais à uma constante que chamaremos de $-\lambda$. 
E a equação passa a ser o sistema baixo
	$$\begin{cases} X''(x)+\lambda X(x)=0\\T'(t)+\lambda kT(t)=0\end{cases}$$
Vamos analisar casos de $\lambda$
1) $\lambda =0$, produz uma solução trivial em que tudo é 0. Não interessa
2) $\lambda <0$ Não produz solução
3) $\lambda >0$, Produz a solução $\displaystyle X_n(x) = C_n sen\left( \frac{n\pi}{L}\right)$ e $\displaystyle T_n(t)= B_n exp \left( -\frac{n^2 \pi^2 k}{L^2} \right)$  
	Com solução geral $\displaystyle u_(x,t) = \sum_{n=1}^\infty A_n sen\left(\frac{n \pi x}{L} \right) exp\left( -\frac{n^2 \pi^2 k t}{L^2}\right)$
	Usando a condução de contorno da temperatura inicial no instante t=0
	$\displaystyle f(x) = u(x,0) = \sum_{n=1}^\infty A_n sen\left( \frac{n \pi x}{L}\right)$
	E para calcular fazemos a extensão por da função e encontramos
	$\displaystyle A_n = \frac{1}{L}\int_{-L}^L F_{\text{exten ímpar}}(x) sen\left( \frac{n \pi x}{L} \right)dx = \frac{2}{L}\int_{-L}^L f(x) sen \left( \frac{n \pi x}{L}\right)dx$  

Para as condições criadas, existia um fluxo de calor pelas extremidades da barra.
Agora consideramos a condição de não ocorrer troca 
#### **[[Condições de Neumann]]**
- nessas condições temos $u_x(0, t) = u_x(L, t)=0$

$\displaystyle u(x,t) = A_0 + \sum_{n=1}^\infty A_n cos \left( \frac{n \pi x}{L}\right) exp \left( - \frac{n^2 \pi^2 k t}{L^2}\right)$ 
$\displaystyle A_0 = \frac{2}{L}\int_0^L f(x)dx$
$\displaystyle A_n = \frac{2}{L} f(x)cos \left( \frac{n \pi x}{L}\right)dx$
