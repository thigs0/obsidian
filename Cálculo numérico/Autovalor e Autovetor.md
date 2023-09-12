Podemos calcular o [[Autovetor]] e [[Autovalor]] de forma computacional
- Algoritmo
	Octave
```octave
function [lambda,x,iter,err] = eigpower(A,tol,nmax,x0)

%Eigpower calcular numericamente um valor próprio de uma matriz
% Lambda = eigpower(A), calcula com o método da potência o autovalor de a
%Lambda = eigpower(A,tol.nmax,xo) usa uma tolerância sobre o valor absoluto do erro tol, nmax é o numero máximo de operações, xo é o vetor inicial
%

[n,m] = size(A)
if n~=m; error("Só para matrizes quadradas"); end

if nargin == 1
	tol = 1.e-06;
	x0 = ones(n,1);
	nmax = 100;
end

x0 = x0/norm(x0); #normaliza o vetor
pro = A*x0;
lambda = x0'*pro;
err = tol*abd(lambda)+1;
iter = 0;
while err> tol*abs(lambda) & abs(lambda) ~=0 & iter <= nmax
	x = pro; x = x/norm(x);
	pro = A*x; lambdanew = x'*pro;
	err = abs(lambdanew - lambda);
	lambda = lambdanew;
	iter = iter + 1;
end
return
endfunction

```