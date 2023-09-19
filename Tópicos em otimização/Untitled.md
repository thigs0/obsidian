Temos uma tabela grande como 

$f:\mathbb{R}\to R_+$
$\displaystyle f(x)=\sum_{j=1}^N [sinal(v_j-x_1-x_2u_j)+w_j]$ 

Como a função sinal não é derivável, aproximamos sempre por uma sigmoide de modo

```functionplot
---
title: Função sigmoide e arcotangente 
disableZoom: false
bounds: [-3, 3, -2, 2]
grid: true
xLabel: x
yLabel: y
---

f(x) = 1/(1+E^(-3*x))
g(x) = (2/PI)*atan(x)

```

Agora aproximamos  $\displaystyle f(x)=\sum_{j=1}^N [sinal(v_j-x_1-x_2u_j)+w_j]\approx \sum_{j=1}^N [atan(x_1+x_2u_j-v_j)+\frac{\pi}{2}w_j]^2$

```julia
using CSV
using DataFrames
using LinearAlgebra

#abre os dados e capta o u, v
csv = CSV.File("/home/cpa/Documentos/tarefa3")
csv = DataFrame(csv)
global u = csv[:, 2];
global v = csv[:, 3];
global w = csv[:, 4];
global n = length(u);
global g = zeros(2)

function fun(x)
	aux1 = x[1] .+ x[2].*u-v
	aux2 = atan.(aux1)+0.5*pi*w;
	f = 0.5*sum(aux1.*aux2)
	aux3 = aux2./(1 .+ aux1.*aux1);
	g[1] = sum(aux3)/n
	g[2] = sum(aux3.*u)/n
	return f, g
end

function minimizador_lucio(x0, f, M, α=10e-4, σ=0.5, ε=10e-9)
    x_ant = copy(x0)
    x_pos = copy(x0)
    k=0; 
	fx, g_pos = f(x);
    g_pos = copy(g_ant);
    η = norm(g_pos, Inf) 

    while (η >= ε) && (k < M)
        if k==0
            t=1
        else
            t = norm(x_pos-x_ant, 2)/norm(g_pos-g_ant, 2)
        end
        w = α*(g_pos')*g_pos;
        fx, g_pos = f(x_pos)
        
        while f(x_pos-t*g_pos) > fx-t*w
            t =  σ*t;
        end
        g_ant = copy(g_pos)
        x_ant = copy(x_pos);
        x_pos = x_pos-t*g_pos;
        η = norm(g_pos, Inf);
        k = k+1
    end
    return x_pos;
end

x = [7; 4];
r = minimizador_lucio(x, fun, 100)
```