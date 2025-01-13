- Simetrias e quantidades conservativas

Extremizamos a dinâmica de um sistema extremizando a ação
$$S=\int_{t_a}^{t_b}L\left(\vec g ,\frac{d\vec a}{dt},t\right)$$
em que $\vec g :\text{Coordenadas generalizadas vetor com n componentes}$
Seja $X(\vec g, t)$ uma [[função]] escalar e $\vec \Psi (\vec g, t)$ uma função vetorial de n componentes. Definimos uma transformação infinitesimal como
$$\begin{align} t\to t'=t+\epsilon X(\vec g(t),t) \\ \vec g(t)\to \vec g(t)+\epsilon \vec \Psi (\vec g(t),t)\\ \epsilon:\text{infinitesimal}\end{align}$$
Dizemos que a integral de ação permanece invariante sob essa transformação se
$$\Delta S=\int_{t_1'}^{t_2'}L\left(\vec g(t), \frac{d\vec g(t')}{dt'}, t'\right)-\int_{t_1}^{t_2}L\left( \vec g(t), \frac{\vec g(t)}{dt},t \right)dt;~~~\forall t_1,t_2,\epsilon$$

#### Teorema
Seja $L\left(\vec g,\frac{d\vec g}{dt},t\right)$ a [[Lagrangiana]] de um sistema mecânico com n graus de liberdade. Se a ação permanece invariante sob a transformação infinitesimal acima, então a quantidade.
$$C=\sum\limits_{i=1}^n \frac{\partial L}{\partial \dot g_i}\left( \dot g_i X-\Psi_i \right)-LX$$
é uma constante de movimento

**Demonstração**
