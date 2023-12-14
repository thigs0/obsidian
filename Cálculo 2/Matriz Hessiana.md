Matriz hessiana é uma [[Matriz]] que nos permite conferir a curvatura de uma função. Para isso usamos [[Derivada Parcial]] em suas componentes e $f\in C^2$

$$\nabla^2f(x)=H[f(x_1,x_2,x_3,...,x_n)]=\begin{bmatrix}\frac{\partial^2f}{\partial x_1^2} & \frac{\partial^2f}{\partial x_1 \partial x_2} & ... & \frac{\partial^2f}{\partial x_1 \partial x_n} \\ \frac{\partial^2f}{\partial x_2 \partial x_1} & \frac{\partial^2f}{\partial x_2^2} & ... & \frac{\partial^2f}{\partial x_2\partial x_n} \\ ... & ... & ... & ... \\ \frac{\partial^2f}{\partial x_n \partial x_1} & \frac{\partial^{2}f}{\partial x_n \partial x_2} & ... & \frac{\partial^2f}{\partial x_n^2}\end{bmatrix}$$

Quando temos uma [[função]] com duas va,
 riáveis, a [[Matriz]] fica na forma:

$$\large \displaystyle \begin{vmatrix} \frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial y \partial x} \\ \frac{\partial^2 f}{\partial x \partial y} & \frac{ \partial ^2 f}{\partial y^2}\end{vmatrix}$$

**Exemplo**
$f(x)=x_1\sin(x_2)+x_2e^{x_1}$
$\nabla f(x)=\begin{bmatrix} \sin(x_2)+x_2e^{x_1} & x_1\cos(x_2)+e^{x_2}\end{bmatrix}$
$\nabla^2 f(x)\begin{pmatrix}x_2e^{x_1} & cos(x_2)+e^{x_1} \\ cos(x_2)+e^{x_1} & -x_1\sin(x_2)\end{pmatrix}$

**Propriedades**
- A matriz é sempre quadrada de nxn
- Se as [[Derivada segunda]]s são [[Contínua]]s, então a matriz é uma [[Matriz simétrica]] 