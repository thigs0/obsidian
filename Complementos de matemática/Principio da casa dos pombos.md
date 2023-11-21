Temos n casinha e $n+1$ pombos, colocar os pombos nas casinha, pelo menos uma casinha terá 2 pombos

**Demonstração** Por absurdo, Suponhamos que em cada casa não exista mais do que k pombos, então, contando todos os pombos contidos nas N casas não teremos mais do que N k pombos, contrariando a hipótese de termos N k +1 pombos distribuídos nas N casas.

caso queiramos dividir m objetos em  n casas temos
$\displaystyle \lfloor{\frac{m}{n}}\rfloor$ como se esse número não é inteiro, somamos um. O que nos daria a função $$\lceil \frac{m}{n} \rceil$$
Uma generalização probabilística do princípio da casa dos pombos define que se $n$ pombos são colocados aleatoriamente em $m$ casas com uma [[Distribuição uniforme]] $1/m$, então pelo menos uma casa de pombos terá mais de um pombo com probabilidade.
$$1-\frac{m!}{(m-n)!m^n}$$