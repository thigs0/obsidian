Considerando a tarefa abaixo ![[tarefa1.pdf]]
A solução em código está em
```julia
using LinearAlgebra
using Plots #Constroi os gráficos
using Calculus #Biblioteca que calcula gradiente e derivada

function minimizador(x0, f, M, α=10e-4, σ=0.5, ε=10e-9)
    x = copy(x0)
    k=0; g_ant= Calculus.gradient(f, x);
    g_pos = copy(g_ant);
    η = norm(g_pos, Inf) 

    while (η >= ε) && (k < M)
        t = 1; w = α*(g_pos')*g_pos;
        while f(x-t*g_pos) > f(x)-t*w
            t =  σ*t;
        end
        x = x-t*g_pos;
        g_ant=g_pos;
        g_pos = Calculus.gradient(f, x)
        η = norm(g_pos, Inf);
        k = k+1
    end
    return x;
end

function minimizador_lucio(x0, f, M, α=10e-4, σ=0.5, ε=10e-9)
    x_ant = copy(x0)
    x_pos = copy(x0)
    k=0; g_ant= Calculus.gradient(f, x_pos);
    g_pos = copy(g_ant);
    η = norm(g_pos, Inf) 

    while (η >= ε) && (k < M)
        if k==0
            t=1
        else
            t = norm(x_pos-x_ant, 2)/norm(g_pos-g_ant, 2)
        end
        w = α*(g_pos')*g_pos;
        fx = f(x_pos)
        while f(x_pos-t*g_pos) > fx-t*w
            t =  σ*t;
        end
        x_ant = copy(x_pos);
        x_pos = x_pos-t*g_pos;
        g_ant = copy(g_pos)
        g_pos = Calculus.gradient(f, x_pos)
        η = norm(g_pos, Inf);
        k = k+1
    end
    return x_pos;
end

function quadratica(x)
    y = 0
    x = x.^2
    for i in 1:length(x)
        y += i*x[i]
    end
    y /= 2
    return y
end

function Rosenbrock(x)
    y=0
    for i in 1:Int((length(x)/2))
        y += 10*(x[2*i]-x[2*i-1]^2)^2 + (x[2*i-1]-1)^2
    end
    return y
end


x = [7; 4; 3; 25; 4; 300; 4; 100; 7; 10];
x_esp = zeros(length(x))
D = 100 #max de iterações
y_normal = zeros(D);
y_lucio = zeros(D);

for i in 1:D
    y_normal[i] = norm(x_esp - minimizador(x, quadratica, i))
    y_lucio[i] = norm(x_esp - minimizador_lucio(x, quadratica, i))
end

a = plot(1:D, y_normal, label="Dados gerados normalmente", yaxis=:log, title="Gráfico da minimização da função quadrática")
plot!(1:D, y_lucio, label="Dados com melhoria", yaxis=:log)
savefig(a, "min_quadratica.png")

x_esp = ones(length(x))
for i in 1:D
    y_normal[i]= norm(x_esp - minimizador(x, Rosenbrock, i))
    y_lucio[i] = norm(x_esp - minimizador_lucio(x, Rosenbrock, i))
end

display(minimizador_lucio(x, Rosenbrock, 10000000))
a = plot(1:D, y_normal, label="Dados gerados normalmente", title="Gráfico da minimização da função Rosenbrock")
plot!(1:D, y_lucio, label="Dados com melhoria")
savefig(a, "min_rosenbrock.png")
```

No código acima construi duas funções que acham os [[Minimizador]]es
*Minimizador* e *Minimizador_lucio*. A primeira considera o código como descrito no problema e a segunda considera o valor de t como uma função do [[Gradiente]].
Em seguida foram construídas as funções de Rosenbrock e uma quadrática
Considerei o ponto inicial $x_0 = \begin{pmatrix}7 & 4 & 3 & 25 & 4 & 300 & 4 & 100 & 7 & 10\end{pmatrix}$ 
Para analisar a convergência, foi construído um gráfico do número de iterações pela norma do vetor diferença
![[min_quadratica.png|400|center]]
![[min_rosenbrock.png|400|center]]

