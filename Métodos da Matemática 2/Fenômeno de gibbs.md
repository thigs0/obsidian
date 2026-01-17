
**Demonstração**

### Para uma função degrau em \( x = 0 \):

$$
f(x) = \begin{cases}
-1 & \text{se } -\pi < x < 0 \\
1 & \text{se } 0 < x < \pi
\end{cases}
$$

### Série de Fourier:

$$
S_N(x) = \frac{4}{\pi} \sum_{k=1}^{N} \frac{\sin((2k-1)x)}{2k-1}
$$
![[fourier_many_n.png|600]]

é possível analisar o maior valor da [[Séries de Fourier]] conforme avançamos no valor n de aproximação

| Índice (n) | Valor da Aproximação |
| ---------- | -------------------- |
| 0          | 0.00000000           |
| 1          | 1.07139413           |
| 2          | 1.20039916           |
| 3          | 1.18829487           |
| 4          | 1.18410375           |
| 5          | 1.18226800           |
| 6          | 1.18100214           |
| 7          | 1.18062464           |
| 8          | 1.18028056           |
| 9          | 1.17995047           |
| 10         | 1.17974479           |
| 11         | 1.17925274           |
| 12         | 1.17825526           |
| 13         | 1.17793520           |
| 14         | 1.17851516           |
| 15         | 1.17929098           |
| 16         | 1.17853569           |
| 17         | 1.17818223           |
| 18         | 1.17878606           |
| 19         | 1.17812500           |
e é possível ver que aparentemente o valor converge para próximo de 1.17

```python
# Exemplo simples do Fenômeno de Gibbs
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-np.pi, np.pi, 1000)
f = np.sign(x)  # Função degrau

# Série de Fourier truncada
def S_N(x, N):
    result = np.zeros_like(x)
    for k in range(1, N+1):
        result += np.sin((2*k-1)*x) / (2*k-1)
    return (4/np.pi) * result

plt.figure(figsize=(10, 6))
plt.plot(x, f, 'k-', linewidth=2, label='Função original')
for N in [5, 20, 100]:
    plt.plot(x, S_N(x, N), '--', label=f'N = {N}', alpha=0.8)
plt.legend()
plt.title('Fenômeno de Gibbs - Convergência em Descontinuidades')
plt.grid(True)
plt.show()