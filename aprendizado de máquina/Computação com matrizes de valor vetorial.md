
Redes MLPs de valor vetorial (V-MLPs)

**Camada Densa**
Uma camada densa de valor vetorial é uma aplicação $D:\mathbb{V}\to\mathbb{V}^m$ dada por $$D(x)=\Psi(Wx+b)$$
em que $\mathbb{V}$ é uma álgebra caracterizada por uma tabela de multiplicação associada à $p\in \mathbb{R}^{n\times n\times n}$. $\Psi :\mathbb{V}\to \mathbb{V}$ é uma função de ativação de valor vetorial $W\in \mathbb{V}^{M\times N}$ é a [[Matriz]] dos pesos sinápticos e $b\in \mathbb{V}^M$ é o [[Vetor]] dos viéses (bias).
Na prática, vamos trabalhar em $\varphi(x)$ e a representação real da saída. Dessa forma , temos
$$D(\varphi(x))=\psi_{\mathbb{R}}(\varphi(W)\varphi(x)+\varphi(b))$$
Se $\Psi :\mathbb{V}\to \mathbb{V}$ for uma [[Função split]], ou seja$$\Psi(x)=\sum\limits_{i=1}^n \psi(x_i)e_i,~x=\sum\limits_{i=1}^n x_ie_i$$
Em todo caso
$M_L(W)=\sum\limits_{}^{}$
