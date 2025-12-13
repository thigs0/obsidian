Seja $X_{(1)}=\min{X_1,X_2,...,X_n}$ o mínimo de uma sequência de [[Variável Aleatória]]
$$F_{X_{(1)}}(x)=1-\prod_{i=1}^n [1-F_{X_i}(x)]$$
$F_{X_{(1)}}=P(X_{(1)}<x)$, significa que o mínimo é menor que x, mas não sabemos sobre os outros termos. Neste caso o complementar é mais simples
$F_{X_{(1)}}= 1 - P(X_{(1)}>x)$, Assim todos os termos são maiores que x pelo mínimo
$F_{X_{(1)}} = 1 - P(X_1>x, X_2>x,...,X_n>x)$ usando que tem [[Independência]]
$F_{X_{(1)}}=1-\displaystyle \prod_{i=1}^n P(X_i>x)=1-\displaystyle \prod_{i=1}^n [1-F_{X}(x)]$ 
