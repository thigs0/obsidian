	1Função perda
$h:S\times S\to R_+$ 
Quero minimizar
$f(x)=\frac{1}{n}\sum_{j=1}^n h(g(u_j,x)_jv_j)$


$x = []$
$\displaystyle \large g(u,x)=x_1+x_2e^{x_3u}$ 

```julia
using CSV
using DataFrames
using LinearAlgebra

#abre os dados e capta o u, v
	csv = CSV.read("/home/cpa/Documentos/data")
	csv = DataFrame(csv)
	global u = csv[:, 1];
	global v = csv[:, 1];
	global N = length(u);
	
function fun(x)
	f=0;g=zeros(N)
	for i in 1:N
		aux1=exp(x[3]*u[j]), aux2=x[2]*aux1;
		aux3 = x[1]+aux2-v[j];
		f = f+aux3*aux3;
		g[1] = g[i]+aux3;
		g[2] = g[2]+aux3*aux1;
		g[3] = g[3]+aux3*u[j]*aux2;
	end
	f = f/(2*N);
	g = g/N;
	return [f, g]
end

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


x = [7; 4; 3; 25];
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
    y_normal[i]= norm(x_esp - minimizador(x, fun, i))
    y_lucio[i] = norm(x_esp - minimizador_lucio(x, fun, i))
end

a = plot(1:D, y_normal, label="Dados gerados normalmente", title="Gráfico da minimização da função Rosenbrock")
plot!(1:D, y_lucio, label="Dados com melhoria")
savefig(a, "min_rosenbrock.png")

```