- integrais impróprias envolvem [[Limite]]s da forma $\displaystyle \lim_{R \to \infty} \int_{-R}^R f(x)dx$
   

Problema é encontrar esta [[Integral]], para resolvê-lá usamos o [[Limite]]
```functionplot
---
title: Função exponencial de -x ao quadrado
disableZoom: false
bounds: [-2, 2, 0, 1]
grid: true
xLabel: x
yLabel: y
---

f(x) = E^(-x^2)

```

I = $\displaystyle \int_0^\infty e^{-(x^2)}$      
I.I = $\displaystyle \int_0^\beta \int_0^\beta e^{-(x^2+y^2)}$, Coordenada polar

$\displaystyle I^2 = \iint e^{-(x^2+y^2)} dxdy =\int_0^{\pi/2}\int_\epsilon^r(\theta) e^{-(r^2)}rdrd\theta = \int_0^{\pi/2} \frac{-e^{-r^2}}{2} r(\theta)-> \epsilon = \frac{1}{2}\int_0^{\pi/2} e^{-r^2(\theta)}d\theta + \frac{\pi}{4}e^{-(\epsilon^2)}$
- Usamos a desigualdade -> $|a+b| \geq |a|-|b|$

