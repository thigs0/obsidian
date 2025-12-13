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


### Overshoot máximo:

$\lim_{N \to \infty} S_N\left(\frac{\pi}{N}\right) \approx 1.08949$ 

**Tradução:** O valor converge para cerca de 1.0895 em vez de 1, resultando em um overshoot de ~8.95%.

## 🔍 Propriedades Importantes

| Propriedade                     | Descrição                                                       |
| ------------------------------- | --------------------------------------------------------------- |
| **Convergência Pontual**        | A série converge para o valor médio no ponto de descontinuidade |
| **Não Diminuição do Overshoot** | A amplitude máxima do overshoot não diminui com $N \to \infty$  |
| **Localização**                 | A largura da região afetada diminui com \( N \) aumentando      |
| **Valor Limite**                | Overshoot ≈ 8.95% do salto da descontinuidade                   |

##  Onde Ocorre

- **Séries de Fourier** em funções com descontinuidades
- **Transformada de Fourier** truncada
- **Filtros digitais** com resposta ao impulso de comprimento finito
- **Reconstrução de sinais** a partir de amostras

### Problemas:
- **Processamento de Sinais:** Ringing em imagens e áudio
- **Análise Numérica:** Erros na reconstrução de funções
- **Engenharia:** Artefatos em filtros digitais

### Soluções Comuns:
- **Filtros de Suavização** (janelas de Hamming, Hanning, etc.)
- **Métodos de Regularização**
- **Uso de funções de base suaves** em vez de senos/cossenos

## 🧪 Demonstração Simples

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