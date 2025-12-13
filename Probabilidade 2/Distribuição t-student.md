- Distribuição [[Contínua]], com [[Simetria]] e $v$ é o grau de liberdade
- Quando $v$ é pequena e cresce , então a distribuição se aproxima da [[Distribuição normal]]
- Encontra a média de uma amostra normal sem saber a média e [[Desvio padrão]]
- Surge do problema de analisar uma série de N amostras, sabendo que elas seguiriam uma distribuição normal. Então 
$N(\mu, \sigma^2)\to t(\mu, \sigma^2,v)$
$T=\frac{Z}{\sqrt{\chi^2_v/v}}$~$t_v=t(0,1;v)$
$T=\frac{Z}{\sqrt{V/v}}=\frac{\frac{V_n(\bar X-\mu)}{\sigma}}{\sqrt{\frac{(n-1)S_n^2}{\sigma^2}/(n+1)}}=\frac{\sqrt{n}(\bar X-\mu)/}{}$
A [[função]] distribuição de probabilidade
$$f(t)=\frac{\Gamma(\frac{v+1}{2})}{\sqrt{v}B(\frac{1}{2},\frac{v}{2})}\left( 1+\frac{t^2}{v} \right)^{-\frac{v+1}{2}}$$

---
Seja a média $\bar{X_n}=\frac{X_1+X_2+...+X_n}{n}$
Com [[Variância Amostral]] $\displaystyle S^2_n=\frac{1}{n-1}\sum\limits_{i=1}^2 (X_i-\bar{X_n})^2$ 
A [[Variável Aleatória]] definida como $\displaystyle t=\frac{\overline{X_n}-\mu}{S_n/\sqrt{v}}$ 




#### Avaliação de uma [[Distribuição normal]] em [[Python]]
```python
import numpy as np
from matplotlib import pyplot as plt
import random
#####
N = 5000
values = np.zeros(N)
for i in range(N):
    values[i] = random.normalvariate()
plt.hist(values, bins=300)

t = (mean - 0) / (Ssq / np.sqrt(N))
```

![[norm.png]]


**Tabela t Student**

| v\p      | 0,6   | 0,7   | 0,8   | 0,9   | 0,95  | 0,975  | 0,98   | 0,99   | 0,995  |
| -------- | ----- | ----- | ----- | ----- | ----- | ------ | ------ | ------ | ------ |
| 1        | 0,325 | 0,727 | 1,376 | 3,078 | 6,314 | 12,706 | 15,895 | 31,821 | 63,657 |
| 2        | 0,289 | 0,617 | 1,061 | 1,886 | 2,92  | 4,303  | 4,849  | 6,965  | 9,925  |
| 3        | 0,277 | 0,584 | 0,978 | 1,638 | 2,353 | 3,182  | 3,482  | 4,541  | 5,841  |
| 4        | 0,271 | 0,569 | 0,941 | 1,533 | 2,132 | 2,776  | 2,999  | 3,747  | 4,604  |
| 5        | 0,267 | 0,559 | 0,920 | 1,476 | 2,015 | 2,571  | 2,757  | 3,365  | 4,032  |
| 6        | 0,265 | 0,553 | 0,906 | 1,44  | 1,943 | 2,447  | 2,612  | 3,143  | 3,707  |
| 7        | 0,263 | 0,549 | 0,896 | 1,415 | 1,895 | 2,365  | 2,517  | 2,998  | 3,499  |
| 8        | 0,262 | 0,546 | 0,889 | 1,397 | 1,86  | 2,306  | 2,449  | 2,896  | 3,355  |
| 9        | 0,261 | 0,543 | 0,883 | 1,383 | 1,833 | 2,262  | 2,398  | 2,821  | 3,250  |
| 10       | 0,26  | 0,542 | 0,879 | 1,372 | 1,812 | 2,228  | 2,359  | 2,764  | 3,169  |
| 11       | 0,26  | 0,54  | 0,876 | 1,363 | 1,796 | 2,201  | 2,328  | 2,718  | 3,106  |
| 12       | 0,259 | 0,539 | 0,873 | 1,356 | 1,782 | 2,179  | 2,303  | 2,681  | 3,055  |
| 13       | 0,259 | 0,538 | 0,870 | 1,35  | 1,771 | 2,160  | 2,282  | 2,650  | 3,012  |
| 14       | 0,258 | 0,537 | 0,868 | 1,345 | 1,761 | 2,145  | 2,264  | 2,664  | 2,977  |
| 15       | 0,258 | 0,536 | 0,866 | 1,341 | 1,753 | 2,131  | 2,249  | 2,602  | 2,947  |
| 20       | 0,257 | 0,533 | 0,86  | 1,325 | 1,725 | 2,086  | 2,197  | 2,528  | 2,845  |
| 30       | 0,256 | 0,53  | 0,854 | 1,31  | 1,697 | 2,042  | 2,147  | 2,457  | 2,75   |
| 40       | 0,255 | 0,529 | 0,851 | 1,303 | 1,684 | 2,021  | 2,123  | 2,423  | 2,704  |
| 60       | 0,254 | 0,527 | 0,848 | 1,296 | 1,671 | 2      | 2,099  | 2,39   | 2,66   |
| 120      | 0,254 | 0,526 | 0,845 | 1,289 | 1,658 | 1,98   | 2,076  | 2,358  | 2,617  |
| $\infty$ | 0,253 | 0,524 | 0,842 | 1,282 | 1,645 | 1,96   | 2,054  | 2,326  | 2,576  |
