1) Hipótese: $f:\mathbb{R}-\{0\} \to \mathbb{R}$, $f(a)=1/(1+e^{1/x})$
Tese: $\lim_{x\to 0^+}f(x)=0$ e $\lim_{x\to 0^-}f(x)=1$ 

Seja $X=\mathbb{R}-\{0\}$ 
$a\in X_+'$, sabemos que f(x) é extritamente crescente pelo comportamento monótono de 1/x e $e^{1/x}$

$\forall \epsilon >0, \exists \sigma>0; 0<|f(x)-0|<\delta$
Tome $a<x$; $f(a)=\frac{1}{1+e^{1/a}}$ 
$|f(x)-0|<\delta \Rightarrow |1/[1+e^{1/x}]|<\delta$ 
$\displaystyle \frac{1}{|1+e^{1/x}|}<\delta\Rightarrow \frac{1}{\delta}-1<e^{1/x}\Rightarrow \frac{1-\delta}{\delta}<e^{1/x}$
$\ln(1-\delta)-\ln(8)<1/x\Rightarrow x<\frac{1}{\ln(1-\delta)-\ln(8)}$
Assim, tome $\epsilon = \frac{1}{\ln(1-\delta)-\ln(8)}$ que as condições são safisteitas

2) Hipótese: $f:X\to \mathbb{R}$, $a\in X'$ e $Y=f(X-\{0\})$  se $Lim_{x\to 0}f(x)=L$
Tese: $L\in \bar Y$

Como o limite existe => $\exists (x_n)\to a$, $x_n\in X-\{0\}$ com $\lim f(x_n)= L$ portanto $L\in \bar Y$

3) Seja $f:A\to \mathbb{R}$, $A\subset \mathbb{R}$ sendo aberto e contínua <=> $\forall c\in \mathbb{R}, ~~E[f<c]$ $E[f>c]$ são abertos
Seja $a\in A,\forall \delta>0$, $(a-\delta,a+\delta)\in A,~~ \exists \epsilon >0, (L-\epsilon,L+\epsilon)\in f(A)$ visto que $\lim f(x)=L$ 

Se $x\notin A$ temos $Z_1=[f<c]$ e $Z_2=[f>c]$ e $\forall \epsilon>0$ e $a\in Z_1\Rightarrow (a-\epsilon,a+\epsilon)\in Z_1$
tal que $a+\epsilon \neq c$ e $a=\epsilon \neq c$ então $Z_1$ é aberto. O mesmo vale para $Z_1$ 

4) $A\subset \mathbb{R}$ é aberto
$f:A \subset \mathbb{R}$ é contínua <=> $f^{-1}$ é aberto $\forall B\subset \mathbb{R}$ aberto
Provando =>
$f:A\to B$ , $a\in A$ então $\exists \epsilon>0; (a-\epsilon , a+\epsilon)\in A$ e por f ser contínua então dado a,$\epsilon$.
temos $(f(a-\epsilon),f(a+\epsilon))\in B$
Assim $\forall \epsilon >0,a\in A; (a-\epsilon , a+\epsilon)\subset A$ 
=> $\exists \delta >0,b\in B; (f(a-\epsilon),f(a+\epsilon))\subset (b-\delta,b+\delta)\subset B$ e a união desses intervalos abertos forma um aberto
Provando <= 

5) $\lim \frac{f(y_n)-f(x_n)}{y_n-x_n}=\lim \frac{f(y_n)}{y_n-x_n}- \frac{f(x_n)}{y_n-x_n}$ com a tem uma vizinhança
$\exists \epsilon_11>0, \epsilon_2>0$; $y_n=a+\epsilon_1$ e $x=a-\epsilon_2$
=> $\lim \frac{f(a+\epsilon_1)}{a+\epsilon_1-a+\epsilon_2}-\frac{f(a-\epsilon_2)}{a+\epsilon_1-a+\epsilon_2}=\lim \frac{f(a=\epsilon_1)-f(a-\epsilon_2)}{\epsilon_1+\epsilon_2}= \lim_{h\to 0} \frac{f(a+h-\epsilon_2)-f(a-\epsilon_2)}{h}$
como $\lim x_n=\lim y_n=a$ => $\epsilon_{2,n}\to 0$ quando $n\to \infty$ de forma que nos aproximamos de $\frac{f(a+h)-f(a)}{h}$ porém $h=\epsilon_2+\epsilon_1$; $h\to 0$ então $\lim [f(a+h)-f(a)]/h=f'(a)$ 

6) vrv

7) Seja p(x)o polinômio então ele pode ser escrito como $p(x)=\sum\limits_{i=1}^n a_{i}x^{i}$ tal que i sempre é ímpar e $p\in X^2$ então sua derivada pode ser expressa como $p''(x)=\sum\limits_{i=0}^n a_ii(i-1)x^{i-2}$  e i-2 é um número ímpar.
   Para todo polinômio ímpar temos $\lim_{x\to \infty} p''(x) = \infty$ e $\lim_{x\to -\infty} p''(x)=-\infty$ Então pelo teorema de Bolzano-Waistrass $\exists c\in \mathbb{R}; ~p''(c)=0$ visto que p é contínua
