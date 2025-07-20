A [[Equação de Bessel]] de ordem $v$ é $$z^2y''+zy'+(z^2-v^2)y=0$$
usando [[Séries de Potências]] com [[Série de Frobenius]] $\displaystyle y=\sum\limits_{n=0}^\infty a_nz^{n+r}$ temos
$$\begin{cases}y=\sum\limits_{n=0}^\infty a_nz^{n+r}\\ y'=\sum\limits_{n=1}^\infty a_n(n+r)z^{n+r-1}\\ y''= \sum\limits_{n=2}^\infty a_n(n+r)(n+r-1)z^{n+r-2}\end{cases}$$
$$z^2\sum\limits_{n=0}^\infty a_n(n+r)(n+r-1)z^{n+r-2}+z\sum\limits_{n=0}^{\infty}a_n(n+r)z^{n+r-1}+(z^2-v^2)\sum\limits_{n=0}^\infty a_nz^{n+r}=0$$
$$\sum\limits_{n=0}^\infty a_n(n+r)(n+r-1)z^{n+r}+\sum\limits_{n=0}^\infty a_n(n+r)z^{n+r}+\sum\limits_{n=0}^\infty a_nz^{n+r+2}-\sum\limits_{n=0}^\infty v^2a_nz^{n+r}=0$$
$$\begin{cases} n=0~~~, (r^2-v^2)a_0=0 \\n=1~~~,a_0r(r-1)+a_0r-v^2a_0=0 \Rightarrow [(r+1)^2-v^2]a_0=0\\ n=n~~~, a_n=\displaystyle \frac{-a_{n-2}}{(n+r)^2-v^2} \end{cases}$$

De modo que 
$v=\pm r$ => $a_1=0$ por $v\neq 0$ 
==> $a_{2k+1},~~\forall k\in \mathbb{N}$ 
==> $a_{2k}=\displaystyle \frac{-a_{(2k)-2}}{2^2k^2-2v} = \frac{-a_{2(k-1)}}{2(2k^2-v)},~\forall k\in \mathbb{N_+}$

Para k=1
$\displaystyle a_2=\frac{-a_0}{2(2-v)}$
Para k=2
$a_{4}=\displaystyle \frac{-a_2}{2(22^2-v)}=\frac{-(-a_0)}{(2(22^2-v))(2(2-v))} = \frac{a_0}{2^2(22^2-v)(2-v)}$
Para k=3
$a_{6} = \displaystyle \frac{-a_4}{2(26^2-v)}=  \frac{-a_4}{2(2^33^2-v)}=\frac{-a_0}{(2(2^33^2-v))(2^2(22^2-v)(2-v))} = \frac{-a_0}{2^3(2^33^2-v)(2^3-v)}$
Para k=4
$a_8=\displaystyle \frac{-a_6}{2(28^2-v)} = \frac{a_0}{2(28^2-v)2^3(2^33^2-v)(2^3-v)} = \frac{a_0}{2^4(2^7-v)(2^33^2-v)(2^3-v)}$
Para k=5
$a_{10}=\displaystyle \frac{-a_8}{2(2(10)^2-v)} = \frac{-a_8}{2(2^25^2 -v)} = \frac{-a_0}{2(2^25^2-v)2^4(2^7-v)(2^33^2-v)(2^3-v)} = \frac{-a_0}{2^5(2^25^2-v)(2^33^2-v)(2^3-v)}$ 

Assim $$a_{2k}=\frac{(-1)^k z^{2k+v}}{2^{2k}k!(v+1)_k}$$
onde $(v+1)_k=(v+1)(v+2)...(v+k)$

- usando a representação em [[Função gama]]
$$J_v(x)=\sum\limits_{n=0}^\infty \frac{(-1)^n}{\Gamma (n+1)\Gamma (n+v+1)}\left( \frac{x}{2} \right)^{2n+v}$$
Este citado é conhecido como Bessel de primeira ordem, com as seguintes propriedades

***Propriedades***
Para $v\in \mathbb{Z}$
- $\displaystyle e^{\frac{x}{2}(t-t^{-1})}=\sum\limits_{m=-\infty}^\infty J_m(x)t^m$ por expansão do euler por [[Polinômio de Taylor]]
- $J_n(x)=(-1)^nx^n\left( \frac{1}{x}\frac{d}{dx} \right)^nJ_0(x)$
**Demonstração**
n=1 => $J_1(x)=-\frac{x}{x}\frac{d}{dx}J_0=-J_0$
n=k => $J_k(x)=(-1)^kx^k\left( \frac{1}{x}\frac{d}{dx} \right)^kJ_0$
n=k+1 => $J_{k+1}=-x^k\frac{d}{dx}\left( \frac{1}{x^k}J_k(x) \right)=-x^k\frac{d}{dx}\left( \frac{x^k}{x^k}(-1)^k\left( \frac{1}{x}\frac{d}{dx} \right)^kJ_0(x) \right)$
= $(-1)^{k+1}x^{k+1}\left( \frac{1}{x}\frac{d}{dx} \right)^{k+1}J_0(x)$
- $\displaystyle \frac{d}{dx}(x^vJ_v)=x^vJ_{v-1}$
- $\frac{d}{dx}(x^{-v}J_v)=-x^{-v}J_{v+1}$
- $J_{v-1}+J_{v+1}=\frac{2v}{x}J_v$
- $J_{v-1}-J_{v+1}=2J'_v$ 