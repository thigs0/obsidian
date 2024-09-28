- Atrito é uma [[Força]] não constante
$f_{at}=\mu |N|$
$\mu \begin{cases}\mu_s~\text{Se não há movimento}\\\mu_d~\text{Há movimento relativo entre os 2 corpos}\end{cases}$
$\mu_s$ mi estático
$\mu_d$ mi dinâmico
$$\mu_d<\mu_s$$
Esta diferença se da pela rugosidade das superfícies.

---
$F=m\frac{dv}{dt}$
=> $\displaystyle v(t)=v_0+\int_0^t \frac{F(t)}{m}dt$
$\displaystyle r(t)=r_0+\int_0^tv(t)dt$

---
##### Força dependente da velocidade
**Exemplo**
Carga elétrica se movendo em um campo eletro-magnético
$F(v) = q(v\times B)$ <== [[Força de Lorentz]]
**Exemplo**
Resistência do ar

$F(v)=-mkv^n \hat v$ , dizemos que é proporcional a [[Velocidade]]
Usando as [[Leis de newton]]
$m\frac{dv}{dt}=-kmv$ -> $\displaystyle \int \frac{dv}{dt}=\int -kv$ -> $\ln v =-kt+C_1$ 
$$v = v_0e^{-kt}$$
Caso integremos, obteremos a posição
$$x=v_0\int e^{-kt}dt=-\frac{v_0}{k}e^{-kt}+C_2$$
Com a condição inicial de $x(t_0)=0$ 
$$x=\frac{v_0}{k}(1-e^{-kt})$$

Caso tenhamos

![[Mecânica Geral/imagem/Untitled Diagram.svg]]

$\Delta p=\Delta p_0\delta A\Delta x=\Delta p_0 \rho Av\Delta t$
$\Delta p=(\Delta p_0 p A)v.\Delta t$ => $\frac{\Delta p}{\Delta t}=-bv$ 

---
Lançamento de uma partícula com resistência do ar
![[Mecânica Geral/imagem/Untitled Diagram 1.svg]]
$m r=m\frac{dv}{dt}=-mg\hat y-bv$
conseguimos rescrever as componentes
$m\ddot x=-b\dot x m$, 
$m\ddot y=-mb\dot y-mg$

- Para componente em $x$
$\ddot x=-b\dot x$ ->    $\dot x=-bx+C$   ->   $x$

- Para compenente y
$\ddot y=-b\dot y-g$  ->  $\dot y=-by-gt$  ->