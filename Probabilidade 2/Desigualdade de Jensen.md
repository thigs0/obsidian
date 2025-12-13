Se $f(x)$ é uma [[Função convexa]], então
$$\mathbb{E}[f(x)]\geq f(\mathbb{E}[X])$$
**Demonstração**
Expandindo na [[Polinômio de Taylor]] em torno de $\mu =\mathbb{E}[X]$, obtemos
$f(x)=f(\mu)+f'(\mu)(x-\mu)+\frac{f''(\Xi)(x-\mu)^2}{2}$ onde $\Xi$ é um valor entre x e $\mu$. Já que $f'(\Xi)\geq 0$, obtemos
$f(x)\geq f(\mu)+f'(\mu)(x-\mu)$
$\mathbb{E}[f(X)]\geq f(\mu)+f'(\mu)\mathbb{E}[X-\mu]=f(\mu)$
