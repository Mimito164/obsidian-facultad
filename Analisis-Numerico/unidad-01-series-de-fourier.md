---
fecha: 2026-03-29 2026-03-29
materia: Analisis-Numerico
unidad: "1"
tema: Series de Fourier, serie trigonometrica de fourier
tags: []
---
# Propiedades generales
- Las series de fourier son mas generales que las series de Taylor
- Desarrollar una funcion en una serie de fourier **implica** escribir a dicha funcion como **combinacion lienal** de las funciones de una **base ortonormal**

Se dice que una funcion es seccionalmente continua
$Sea\ f: [a;b]\to \mathbb{R}$
$$
f\text{ es seccionalmente continua} \iff \text{ tiene un numero finitio de saltos finitos}
$$
- Toda funcion $f$ seccionalmente continua en $[a;b]$ es integrable en $[a;b]$
## Espacio vectorial de funciones seccionalmente continuas
$$
F=\{f/f:[a;b]\to \mathbb{R} \land f\text{ es seccionalmente continua en } [a;b]\}
$$
$B=\{f_{1}(x),f_{2}(x),f_{3}(x),\dots,f_{n}(x),\dots\}$ es base de $F$ si y solo si:
$\forall f \in F:f(x)=k_{1}f_{1}(x)+k_{2}f_{2}(x)+\dots+k_{n}f_{n}(x)+\dots$
$$
\forall f \in F: f(x)=\sum_{n=1}^\infty k_{n}f_{n}(x)
$$
Para el caso de la serie trigonometrica de fourier la base debe ser **ortonormal**
Sea $B=\{v_{1},v_{2},\dots ,v_{n}\}$
$$
B\text{ es ortogonal }\iff \forall v_{i},v_{j}\in B:i\neq j\implies<v_{i}\cdot v_{j}> =0
$$
$$
B\text{ es ortonormal }\iff \forall v_{i},v_{j}\in B:i\neq j\implies<v_{i}\cdot v_{j}> =0 \land ||v_{i}||=1
$$
## Producto interior y norma en el espacio vectorial $F$

$$
<f\cdot g> =\int_{a}^b f(x)\cdot g(x) dx
$$
$$
||f|| =\sqrt{ <f\cdot f> }=\sqrt{ \int_{a}^b f^{2}(x)dx }
$$
## Calculo de los coeficientes de la serie de fourier

$$
\begin{array} \\
f = k_{1}f_{1}+k_{2}f_{2}+\dots+k_{n}f_{n}+\dots \\
<f\cdot f_{n}> = <(k_{1}f_{1}+k_{2}f_{2}+\dots+k_{n}f_{n}+\dots) \cdot f_{n}> \\
<f\cdot f_{n}> = < k_{1}f_{1}\cdot f_{n}>+<k_{2}f_{2}\cdot f_{n}> + \dots +<k_{n}f_{n}\cdot f_{n}> + \dots \\
<f\cdot f_{n}> = k_{1}\underbrace{<f_{1}\cdot f_{n}>}_0 + k_{2}\underbrace{<f_{2}\cdot f_{n}>}_{0} + \dots +k_{n}\underbrace{<f_{n}\cdot f_{n}>}_{1} + \dots
\end{array}
$$
$$
k_{n}= <f\cdot f_{n}> =\int_{a}^b f(x)f_{n}(x)dx
$$
## Base de la serie trigonometrica de fourier
$$
B = \{1,\cos(nx),\sin(nx)/ n\in \mathbb{N}\} 
$$
Esta base es ortogonal pero no es **ortonormal**. Entonces dividimos estos terminos por su norma para que asi sea una base ortonormal.
$$
\mathbf{B'=\left\{ \frac{1}{\sqrt{ 2\pi }}, \frac{\cos(nx)}{\sqrt{ \pi }}, \frac{\sin(nx)}{\sqrt{ \pi }}/ n\in \mathbb{N} \right\}}
$$

$$
Sf(x)=k_{0}\frac{1}{\sqrt{ 2\pi }} + \sum_{n=1}^\infty k_{n}\cdot \frac{\cos(nx)}{\sqrt{ \pi }}+k'_{n}\cdot \frac{\sin(nx)}{\sqrt{ \pi }} 
$$
$$
Sf(x)=\frac{a_{0}}{2}+\sum_{n=1}^\infty a_{n}\cos (nx) + b_{n}\sin (nx)
$$
$$
a_{0}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)dx
$$
$$
a_{n}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)\cos(nx)dx
$$

$$
Sf(x)=k_{0}\frac{1}{\sqrt{ 2\pi }} + \sum_{n=1}^\infty k_{n}\cdot \frac{\cos(nx)}{\sqrt{ \pi }}+k'_{n}\cdot \frac{\sin(nx)}{\sqrt{ \pi }} 
$$
$$
Sf(x)=\frac{a_{0}}{2}+\sum_{n=1}^\infty a_{n}\cos (nx) + b_{n}\sin (nx)
$$
$$
a_{0}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)dx
$$
$$
a_{n}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)\cos(nx)dx
$$
$$
b_{n}=\frac{1}{\pi}\int_{0}^{2\pi}f(x)\sin(nx)dx
$$

### Aclaraciones importantes

- Hasta ahora todo esto sirve para funciones definidas entre $0$ y $2\pi$
- Se puede trabajar con funciones periodicas cuyo periodo es $T=2\pi$
- Se puede trabajar en cualquier parte del periodo de $2\pi$ unidades $\int_{K}^{K+2\pi}$
- $Sf(x)=f(x)$ en todos los puntos de continuidad de $f$
- En las discontinuidades, $Sf(x)$ toma el valor medio del salto.
$$
Sf(x)=\frac{{f^+(x)+f^-(x)}}{2}
$$
- $\frac{a_{0}}{2}$ es el valor medio de la funcion. Esto significa que el area debajo de la constante es igual al que esta encima de la constante dado un intervalo igual al periodo.
## Funciones cuyo periodo no sea $2\pi$

La estrategia para abordar estas funciones es, elegir una parametrizacion de la funcion para que su periodo si sea $2\pi$
$$

$$
$$
f(x)=f(x+T) \overbrace{\implies}^{z=\frac{2\pi}{T}x=\omega x}f(x)=f\left( \frac{T}{2\pi}z \right)=g(z)
$$
$$
S(z)=\frac{a_{0}}{2}+\sum_{n=1}^\infty a_{n}\cos(nz)+b_{n}\sin(nz)
$$
$$
S(x)=\frac{a_{0}}{2}+\sum_{n=1}^\infty a_{n}\cos(n\omega x)+b_{n}\sin(n\omega x)
$$
$$
a_{0}=\frac{1}{L}\int_{-L}^{L}f(x)dx
$$
$$
a_{n}=\frac{1}{L}\int_{-L}^{L}f(x)\cos(n\omega x)dx
$$
$$
b_{n}=\frac{1}{L}\int_{-L}^{L}f(x)\sin(n\omega x)dx
$$
$$
\omega_0 = \frac{2\pi}{T} = \frac{2\pi}{2L} = \frac{\pi}{L} \quad \Rightarrow \quad n\omega_0 = \frac{n\pi}{L}
$$
## Particularidades de funciones par e impar

$$
f\text{ es par} \iff f(x)=f(-x)
$$
$$
f\text{ es impar} \iff f(x)=-f(-x)
$$Entonces
$$
\text{Si } g \text{ es impar}\implies \int_{-a}^a g(x)dx =0
$$
$$
\text{Si } g \text{ es par}\implies \int_{-a}^a g(x)dx =2\int_{0}^ag(x)dx
$$
Aplicado a la serie de fourier
Si $f$ es **par**:
$$
b_{n}=\frac{1}{L}\int_{-L}^L \underbrace{\underbrace{f(x)}_{\text{par}} \underbrace{\sin(n\omega x)}_{\text{impar}}}_{\text{impar}}dx=0
$$
$$
a_{n}=\frac{1}{L}\int_{-L}^L \underbrace{\underbrace{f(x)}_{\text{par}} \underbrace{\cos(n\omega x)}_{\text{par}}}_{\text{par}}dx

=\frac{2}{L}\int_{0}^L f(x)\cos(n\omega x)dx
$$
> Se convierte en una serie de **cosenos**

Si $f$ es **impar**:
$$
a_{n}=\frac{1}{L}\int_{-L}^L \underbrace{\underbrace{f(x)}_{\text{impar}} \underbrace{\cos(n\omega x)}_{\text{par}}}_{\text{impar}}dx

=0
$$
$$
b_{n}=\frac{1}{L}\int_{-L}^L \underbrace{\underbrace{f(x)}_{\text{impar}} \underbrace{\sin(n\omega x)}_{\text{impar}}}_{\text{par}}dx

=\frac{2}{L}\int_{0}^L f(x)\sin(n\omega x)dx
$$
> Se convierte en una serie de **senos**
## Funciones periodicas alternadas
$$
f(x)=-f\left( x+\frac{T}{2} \right)
$$
- Se dice que es periodica alternada o que tiene simetria de media onda
- No necesaria mente es par o impar
- una funcion par o impar puede tener simetria de media onda

### Propiedad
$$
\text{Si } f \text{ es periodica alternada} \implies \text{ los coeficientes de la STF } a_{0}, a_{2k},b_{2k}\text{ son nulos}
$$

Algunas funciones se nos puede facilitar el calculo desplazandolas verticalmente.

$$
f(x)=g(x)+3\quad Sf(x)=Sg(x)+3
$$
### Espectros discretos de la STF
son graficos del valor de $a_{n}$ o $b_{n}$ en funcion de $n$

#### Propiedad
Siempre se cumple que:
$$
\lim_{ n \to \infty } a_{n}=0\quad \lim_{ n \to \infty } b_{n}=0
$$