```julia
using LinearAlgebra
using Calculus

#função quadrática que queremos
function fun(x)
    return sum(x.^2)
end

#função de Rosenbrock
function Rosenbrock(x)
    #n é o limitante de iterações
    n = length(x)
    if ~iseven(n/2)
        error("N need be a even number")
    end
    s = 0.0
    for i in 1:(Int(n/2))
        s += (x[2*i]-x[2*i-1]^2)^2 + (x[2*i-1]-1)^2 
    end
    return s
end

function minimizador(x ,f , α=0.5 ,M=50 ,ε=10e-9)
    #x é o vetor de ponto iniciais
    #f é a função que queremos minimizar
    #
    #M é a quantidade máxima de iterações
    #ε é o quanto queremos de precisão

    k=0
    g = Calculus.gradient(f, x)
    while (norm(g) > ε && k < M)
        d = -g; t=1;
        while f(x+t*d) > f(x)+α*t*g'*d
            t /= 2
        x += t*d
        k += 1
        end
    end
    return x;
end

#Mostra a função
x = [3.0, 2.0, 3.0, 4]
#Rosenbrock(x)
display(minimizador(x, Rosenbrock))
```